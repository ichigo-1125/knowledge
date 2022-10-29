# Rustの基礎知識


## 目次

- [Rustの概要](#rustの概要)
	- [未定義動作](#未定義動作)
	- [並列プログラム](#並列プログラム)
	- [実行速度](#実行速度)
- [Rust開発を支えるツール](#rust開発を支えるツール)
- [ユニットテスト](#ユニットテスト)
- [Rustにできないこと](#rustにできないこと)


## Rustの概要

**Rust**はシステムプログラミングのための言語であり、**C**や**C++**といった言語を置き換える次世代のプログラミング言語となることを目指している。

### 未定義動作

システムプログラミングにおいて一般的に用いられているCやC++といった言語においては、未定義動作を引き起こす危険性がある。**未定義動作**とは、ポータブルでない、もしくは正しくないプログラム構成要素、もしくは正しくないデータを使用した場合の動作である。プログラマはこれらの未定義動作を避けるためのいくつものルールを意識しながらプログラムを作成する必要がある。

Rustはコンパイル時に**ダングリングポインタ**や**メモリの多重開放**、**nullポインタの参照解決**といった未定義動作を検出することができる。そのため、コンパイラのチェックをパスしたプログラムは未定義動作を引き起こさないことが保証されている。これを実現するため、Rustには多くの制約が設けられており、プログラマが習熟するには多くの訓練と経験が必要となる。

### 並列プログラム

CやC++で並列プログラムを書くことは、シングルスレッドコードでは起こり得ないような未定義動作に対しても注意する必要があり、一般的に非常に難しいことが知られている。

Rustでは、安全性のために設けられた制約の副産物として、**データ競合**を避けられるようになっている。データを変更しない限りはデータをスレッド感で共有することが許されているが、変更される可能性があるデータに対しては**排他ロック**や**条件変数**、**チャネル**、**アトミック変数**といった**同期機構**を使ってのみアクセスできる。

### 実行速度

C++には**ゼロオーバーヘッド原則**という、実行することに対して余計なコード（**ガベージコレクタ**（GC）など）でCPUを消費しない、という考え方がある。

Rustには**ゼロコスト抽象化**という、抽象化の処理に最小限のコストしか払わない、という考え方がある。例えば、Rustの抽象型であるtraitはコンパイル時に**静的ディスパッチ**される（具体的な型に置換される）ことで、実行時のオーバーヘッドがない。

このようにRustはC++と同様に、プログラマが計算機の能力を最大限活用できるようなコードを書くことを支える言語である。


## Rust開発を支えるツール

Rustには開発を支える便利なツールが存在する。

**rustup**はRustのインストールやアップデートを支える、RubyのRVMやNodeのNVMのようなツール。

**Cargo**はRustのコンパイルマネージャとパッケージマネージャを兼ね備えるツール。

**rustc**はRustのコンパイラで、多くの場合はCargoによって起動される。

**rustdoc**は、Rustのドキュメンテーションツールで、ソースコード中の**ドキュメンテーションコメント**を整形してHTMLを生成する。


## ユニットテスト

Rustはテスト機構が言語に組み込まれており、ユニットテストを実行するための環境が整えられている。


## Rustにできないこと

Rustは所有権システムにより単純な操作の動作を予測しやすくしているが、高度な操作をしようとした時にC++ほどの柔軟性はない。例として、C++では代入演算子をオーバーロードして特別なコピーや移動コンストラクタを定義することができるが、Rustではそれができない。C++ではごく普通に見えるコードで、暗黙に参照カウントをインクリメントしたり、高価なコピーを後回しにするなどの洗練された実装上のトリックを使うことができる。