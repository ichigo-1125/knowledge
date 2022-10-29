# インターネットの歴史


## 目次

1. [コンピュータとネットワークの発展](#コンピュータとネットワークの発展)
	1. [バッチ処理](#バッチ処理)
	1. [タイムシェアリングシステム](#タイムシェアリングシステム)
	1. [コンピュータ間通信](#コンピュータ間通信)
	1. [コンピュータネットワーク](#コンピュータネットワーク)
	1. [インターネットの普及](#インターネットの普及)
1. [TCP/IPの歴史](#tcpipの歴史)
	1. [軍事技術の応用から](#軍事技術の応用から)
	1. [ARPANETの誕生](#arpanetの誕生)
	1. [TCP/IPの誕生](#tcpipの誕生)
	1. [UNIXの普及とインターネットの拡大](#unixの普及とインターネットの拡大)
	1. [商用インターネットサービスの開始](#商用インターネットサービスの開始)


## コンピュータとネットワークの発展

| 年代     | 概要                            |
| -------- | ------------------------------- |
| 1950年代 | バッチ処理                      |
| 1960年代 | タイムシェアリングシステム(TSS) |
| 1970年代 | コンピュータ間通信              |
| 1980年代 | コンピュータネットワーク        |
| 1990年代 | インターネットの普及            |
| 2000年代 | インターネット技術中心          |

### バッチ処理

処理するプログラムやデータなどを、まとめて一括で処理する方式を**バッチ処理**という。コンピュータが高価だった1950年代には、プログラムやデータを打ち込んだカードやテープを計算機センターに持っていって、後日、実行結果を取りに行くといったことをしていた。

### タイムシェアリングシステム

**タイムシェアリングシステム**（TSS）は、1台のコンピュータに複数の端末を接続して、複数のユーザが同時にコンピュータを利用できるようにしたシステム。1960年代に登場し、それまでとは違いインタラクティブ（対話的）にコンピュータを操作することが可能になった。この当時利用されていたプログラミング言語としては、**BASIC**や**COBOL**、**FORTRAN**などがある。

しかし、あるコンピュータから別のコンピュータにデータを移したいときには磁気テープやフロッピーテープといった外部記録媒体にデータをいったん保存して、物理的に輸送する必要があった。

### コンピュータ間通信

1970年代には、コンピュータ間通信の実現により、利用者の目的や規模に合わせた柔軟なシステムの構築・運用が可能となった。

### コンピュータネットワーク

1970年代～1980年代にかけて、[パケット交換](,/01_basic_knowledge_of_network.md#パケット交換)技術によるコンピュータネットワークの実験が行われた。また、この頃に登場した**ウィンドウシステム**（コンピュータの画面上で複数のウィンドウを開くことができるシステム）は、ネットワークの利便性を劇的に向上させた。

### インターネットの普及

1990年代はじめには、コンピュータの利用がより一般的になり、**ダウンサイジング**や**マルチベンダ接続**（異機種間接続）といった言葉が流行した。このマルチベンダ接続に用いられたのがインターネット通信技術であった。

以前は**閉域網**（**クローズドネットワーク**）の制御ネットワークが利用されることが多かったが、現在はインターネットに接続することが一般的になっている。その代表例として、**サプライチェーンマネジメント**（取引先との間で需要や在庫量の情報を共有して、効率の良い物流を目指すこと）などが挙げられる。


## TCP/IPの歴史

### 軍事技術の応用から

1960年代、大学や各研究所などで新しい通信技術の研究が行われるようになった。その中のひとつに**アメリカ国防総省**（**DoD**: The Department of Defense）が中心になって進められた研究があった。DoDは通信技術に軍事的な価値を見出していたため、堅牢で安全な通信が実現できるように技術を確立していった。

この頃には、通信回路の交換局が攻撃されても経路を迂回して通信が持続できるように**分散型ネットワーク**の必要性が唱えられた。これを実現するために注目されたのが、**パケット通信技術**であった。

### ARPANETの誕生

1969年にパケット交換の実用性を確認するための実験が行われた。この時に構築されたネットワークは、アメリカの大学と研究機関4つのノードを結んだもので、**ARPANET**（Advanced Research Projects Agency Network）と呼ばれた。ARPANETの開発には、**アメリカ国防総省高等研究計画局**（**DARPA**: Defense Advanced Research Projects Agency）が資金援助していた。

この実験により[パケット交換](./01_ネットワークの基礎知識.md#パケット交換)技術が実用に耐えられることが証明された。

### TCP/IPの誕生

ARPANET内の研究グループによって、ARPANETのパケット交換の技術に加えて、相手のコンピュータとの間で信頼性の高い通信手段を提供するプロトコルの開発が行われた。こうして1970年代前半に開発されたのが、**TCP/IP**である。

### UNIXの普及とインターネットの拡大

1980年代前後の大学や研究所では、コンピュータのOSとして**BSD UNIX**が広く使用されていた。このOSの内部にはTCP/IPが実装されていた。

また、LANの発達により、大学や企業の研究所などが徐々にARPANETやその後継である**NSFnet**に接続するようになった。この頃から、TCP/IPによる世界的なネットワークを**インターネット**と呼ぶようになった。

### 商用インターネットサービスの開始

1990年代になると、企業や一般家庭にもインターネットへの接続を提供するサービスが普及した。このようなサービスを提供する会社を**ISP**（インターネットサービスプロバイダ）と呼ぶ。

インターネットの商用利用を許可するISPが登場し、インターネットはさらに急激な速度で普及していくこととなった。