# プログラミング言語と並行性


## 目次

1. [アセンブリ言語](#アセンブリ言語)
	1. [アセンブリ言語の基本](#アセンブリ言語の基本)
	1. [x86-64アセンブリの基礎](#x86-64アセンブリの基礎)
1. [C言語](#c言語)
	1. [Pthreads](#pthreads)
	1. [volatile修飾子](#volatile修飾子)
	1. [スタックメモリとヒープメモリ](#スタックメモリとヒープメモリ)
1. [Rust言語](#rust言語)


## アセンブリ言語

**アセンブリ言語**はCPUの機械語と1対1の関係となっている低水準なプログラミング言語である。

### アセンブリ言語の基本

```
x0 = x1 + x2
```

上の数式は、アセンブリ言語（ここではAArch64）では次のように記述される。

```
add x0 x1 x2
```

`add` は**ニーモニック**と呼ばれ、命令の種類（**オペコード**）を表す。アセンブリ言語の1命令は、命令の種類を表すコードと、計算対象を表すオペランド（定数あるいはレジスタ）からなる。**レジスタ**はコンピュータの中で最もアクセス速度が速く容量が少ない記憶領域である。

アセンブリ言語で書かれたプログラムを**アセンブリコード**、アセンブリコードを機械語にコンパイルするソフトウェアを**アセンブラ**と呼ぶ。

次はアセンブリ言語でメモリアクセスを行う例である。

```
ldr x0, [x1] ; [x1]のメモリの値をx0へ読み込み
str x0, [x1] ; [x1]のメモリへx0の値を書き込み
```

また、値の代入は `mov` 命令で行う。

```
mov x0 x1 ; x1の値をx0にコピー
```

### x86-64アセンブリの基礎

**x86-64アセンブリ**には2種類の記法があるが、ここでは**AT&T記法**を用いる。次はx86-64アセンブリで加算は次のように行う。

```
addl %ebx, %ecx ; ebxとecxを足して結果をecxに保存
```

`l` は**オペレーションサフィックス**と呼ばれており、ここにはレジスタのサイズを指定する。

以下はレジスタのコピーの例である。書き込み先レジスタのことを**デスティネーションレジスタ**、書き込み元レジスタのことを**ソースレジスタ**と呼ぶ。

```
movq %rbx, %rcx ; rbxの値をrcxにコピー
```

また、x86-64では、メモリの読み書きも `mov` 命令で可能である。

```
movq (%rbx), %rax ; rbxの指すメモリ上のデータをraxに転送
movq %rax, (%rbx) ; raxの値をrbxの指すメモリに転送
```


## C言語

現在主流のOSは**C言語**で実装されており、マルチスレッド用のライブラリであるPthreadsもC言語のAPIが基本となっている。

### Pthreads

**Pthreads**はPOSIX標準のインタフェースを備えるスレッドライブラリの総称で、LinuxやBSDなどのUNIX系のOSで利用可能であり、Windows実装も存在する。

以下はスレッドの生成と終了待ち合わせの例である。

```c
#include <pthread.h>
#include <stdio.h>
#include <stdlib.h>
#include <unistd.h>

//	スレッド数
#define NUM_THREADS 10

//	スレッドを利用する関数
void* thread_func( void* arg_ )
{
	int id = (int)arg_;
	for( int i=0; i<5; i++ )
	{
		ptinrf("id = %d, i = %d\n", id, i);
		sleep(1);
	}

	return "finished";
}

//	メイン関数
int main( int argc_, char* argv[] )
{
	//	スレッド
	pthread_t v[NUM_THREADS];

	//	スレッド生成
	for( int i=0; i<NUM_THREADS; i++ )
	{
		if( pthread_create(&v[i], thread_func, (void*)i) != 0 )
		{
			perror("pthread_create");
			return -1;
		}
	}

	//	スレッド終了を待機
	for( int i=0; i<NUM_THREADS; i++ )
	{
		char* ptr;
		if( pthread_join(v[i], (void**)&ptr) == 0 )
		{
			printf("msg = %s\n", ptr);
		}
		else
		{
			perror("pthread_join");
			return -1;
		}
	}

	return 0;
}
```

次は、スレッドの終了を明示的に待機せずに自動的にスレッドのリソースを開放するようにする**スレッドデタッチ**の例である。

```c
#include <pthread.h>
#include <stdio.h>
#include <stdlib.h>
#include <unistd.h>

//	スレッドを利用する関数
void* thread_func( void* arg_ )
{
	for( int i=0; i<5; i++ )
	{
		ptinrf("i = %d\n", i);
		sleep(1);
	}

	return NULL;
}

//	メイン関数
int main( int argc_, char* argv[] )
{
	//	アトリビュート初期化
	pthread_attr_t attr;
	if( pthread_attr_init(&attr) ) != 0 )
	{
		perror("pthread_attr_init");
		return -1;
	}

	//	デタッチスレッドに設定
	if( pthread_attr_setdetachstate(&attr, PTHREAD_CREATE_DETACHED) != 0 )
	{
		perror("pthread_attr_setdetachstate");
		return -1;
	}

	//	アトリビュート指定してスレッド生成
	pthread_t th;
	if( pthread_create(&th, &attr, thread_func, NULL) != 0 )
	{
		perror("pthread_create");
		return -1;
	}

	//	アトリビュート破棄
	if( pthread_attr_destroy(&attr) != 0 )
	{
		perror("pthread_attr_destroy");
		return -1;
	}

	sleep(7);

	return 0;
}
```

### volatile修飾子

**volatile修飾子**を利用すると、コンパイラに最適化を抑制したメモリアクセスを実現することができる。メモリアクセスはレジスタアクセスに比較して遅いため、コンパイラはメモリアクセスを抑制するために、レジスタにいったんコピーしてから値を利用する。しかし、メモリ上の値を監視したりする場合にはこの最適化が障害になる場合がある。

次のソースコードはあるメモリ上の値が非ゼロとなるまで待機するCのコードである。

```c
void wait_while_0( int* p )
{
	while( *p == 0 ) {}
}
```

このコードをアセンブリコードで表すと次のようになる。

```
wait_while_0:
	ldr w8, [x0] ; w8にメモリから読み込み
	cbz w8, .LBB0_2 ; if w8 == 0 then goto .LBB0_2
	ret
.LBB0_2
	b .LBB0_2 ; goto .LBB0_2
```

これは結果が0となると `.LBB0_2` にジャンプして無限ループしてしまう。次のコードはvolatile修飾子を用いてメモリアクセスを抑制するコードとなる。

```c
void wait_while_0( volatile int* p )
{
	while( *p == 0 ) {}
}
```

このときのアセンブリコードは次のようになる。

```
wait_while_0:
.LBB0_1:
	ldr w8, [x0] ; w8にメモリから読み込み
	cbz w8, .LBB0_1 ; if w8 == 0 then goto .LBB0_1
	ret
```

### スタックメモリとヒープメモリ

**スタックメモリ**とは関数のローカル変数を保存するためのメモリ領域で、**ヒープメモリ**とは関数のスコープに依存しないようなメモリを動的に確保するためのメモリ領域になる。

```c
int func1()
{
	int a = 10;
	return 2 * func2(a);
}

int func2( int a )
{
	int b = 20;
	return a * b;
}
```

上記のようなコードを実行する場合、 `func1` が呼び出されるとローカル変数 `a` がスタックに保存され、その後 `func2` が呼び出されるとローカル変数 `b` がスタックに積まれる。 `func2` からリターンされるとローカル変数 `b` は解放（破棄）される。ヒープメモリを利用すると関数のスコープに縛られない変数を定義できる。C言語ではヒープメモリの確保と解放は `malloc` と `free` で行える。

```c
#include <stdlib.h>

void fun1()
{
	int a = 10;
	int *b = func2(a);
	free(b);                                //	ヒープメモリ解放
}

int* fun2( int a )
{
	int *tmp = (int*)malloc(sizeof(int));   //	ヒープメモリ確保
	*tmp = a * 20;
	return tmp;
}
```

ヒープメモリ上の領域は明示的に解放するまで確保されたままになるため、解放を忘れると**メモリリーク**と呼ばれるバグの原因となる。


## Rust言語

[詳細は別ノート](../rust)
