# OSI参照モデル


## 目次

1. [OSI参照モデルの概要](#osi参照モデルの概要)
	1. [アプリケーション層](#アプリケーション層)
	1. [プレゼンテーション層](#プレゼンテーション層)
	1. [セッション層](#セッション層)
	1. [トランスポート層](#トランスポート層)
	1. [ネットワーク層](#ネットワーク層)
	1. [データリンク層](#データリンク層)
	1. [物理層](#物理層)


## OSI参照モデルの概要

**OSI参照モデル**は[ISO](./03_standarization_of_tcpip.md#isoとietf)が提唱した、通信[プロトコル](./01_basic_knowledge_of_network.md#プロトコル)を設計するときの指標となるモデル。通信に必要な機能を7つのレイヤに分けて役割を分担することで、ネットワーク[プロトコル](./01_basic_knowledge_of_network.md#プロトコル)の単純化を目的としている。

上位層と下位層の間でやり取りする際の決まりを**インタフェース**、通信相手の同じ階層とやり取りする際の決まり事を**プロトコル**という。

![OSI参照モデル](./img/osi_reference_model.jpg)

### アプリケーション層

**アプリケーション層**は、アプリケーションの中で通信に関係する部分。Webやファイル転送、電子メール、遠隔ログイン（仮想端末）等がある。

### プレゼンテーション層

**プレゼンテーション層**は、アプリケーションが扱う情報を通信に適したデータ形式に変換したり、下位層から来たデータを上位層が処理できるデータ形式にしたりと、データフォーマットに関する責任を負う。

例として、コンピュータ内部でデータをメモリ上に配置する方式で、**ビッグエンディアン方式**と**リトルエンディアン方式**という異なる表現方式がある。このようなコンピュータ内部での表現と、ネットワーク全体での共通表現を変換する。

また、文字コードも同様で、**UTF-8**や**Shift_JIS**、**EUP-JP**など多くの符号化形式がある。

### セッション層

**セッション層**は、コネクション（データの流れる通信路）の確立や切断、転送するデータの切れ目の設定など、データの転送に関する管理を担う。

セッション層よりも下位の層が実際にネットワークを使ってデータの送信処理を行っている。

### トランスポート層

**トランスポート層**は、通信相手のアプリケーションに対して、**確実に**データを届ける責任を負う。データが正しく届いているかを確認したり、届かなかったデータを再送したりする。

### ネットワーク層

**ネットワーク層**は、通信相手までデータを届ける役割を担う。このレイヤでは、どのコンピュータにデータを送ったらよいのかを決定する。

### データリンク層

**データリンク層**は、物理層で直接接続されたノード間での通信を可能にする。直接接続された機器間でのデータのやり取りを実現する。

### 物理層

**物理層**は、ビット列と電圧の高低や光の点滅との相互変換などを行う。
