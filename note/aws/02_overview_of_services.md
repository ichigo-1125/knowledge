# サービス概要


## 目次

1. [コンピューティングサービス](#コンピューティングサービス)
1. [運用支援サービス](#運用支援サービス)
1. [ストレージサービス](#ストレージサービス)
1. [データベースサービス](#データベースサービス)
1. [セキュリティとアイデンティティ](#セキュリティとアイデンティティ)
	1. [AWSアカウントの種類](#awsアカウントの種類)
	1. [AWSアカウント](#awsアカウント)
	1. [IAMポリシー](#iamポリシー)
	1. [IAMユーザとIAMグループ](#iamユーザとiamグループ)
	1. [IAMロール](#iamロール)
1. [アプリケーションサービス](#アプリケーションサービス)
1. [デバロッパツール](#デバロッパツール)
	1. [Codeシリーズ](#codeシリーズ)


## コンピューティングサービス

**コンピューティングサービス**は、アプリケーションを稼働させるインフラストラクチャサービスで、システムアーキテクチャの中核を担う。

**EC2**は、仮想サーバを提供するコンピューティングサービスで、いわゆる[IaaS](../internet/01_basic_knowledge_of_network.md#クラウドの利用)（Infrastructure as a Service）型のサービス。**Elastic Load Balancing**（ELB）や**Auto Scaling**と組み合わせることで、負荷分散を動的に行うことができる。

**ECS**は、Dockerコンテナの実行環境を提供するサービスである。

**Lambda**は、サーバを用意しなくてもプログラムを実行できる環境を提供するサービスである。**サーバレスアーキテクチャ**の中心ともいえるサービスで、拡張性やコスト効率の面でメリットがある。サーバのセットアップやメンテナンスの必要がないため、アプリケーションの開発に集中できる。


## 運用支援サービス

コンピューティングサービスはAWS上にシステムを構築する上で中核となるサービスであったが、AWSにはシステムが世の中に公開されてからの運用フェーズを支援するサービスも存在する。

**Amazon CloudWatch**は、AWSリソースの状態を定期的に取得し、問題があればそれを通知するサービスである。また、独自のトリガーが発生した場合の処理を行う機能も提供されている。

**AWS CloudTrail**は、AWSリソースの作成や、マネジメントコンソールへのログインなどの操作を記録するサービスである。


## ストレージサービス

機械学習やIT技術の革新に伴い、データ量の増加やデータの取り扱い方法の多様化が進んでおり、ストレージサービスの需要は増している。ストレージサービスは以下のように分類できる。

**ブロックストレージ**は、データを物理的なディスクでブロック単位で管理するストレージ。記憶領域をボリュームと呼ばれる単位に分割し、ブロックという単位で呼び出す。データベースや仮想サーバのイメージ保存領域のように、頻繁に更新されたり高速なアクセス必要とされる用途で使われる。**Amazon EBS**がこれにあたる。

**ファイルストレージ**は、ブロックストレージ上にファイルシステムを構成して、データをファイル単位で管理するストレージ。データをファイルとフォルダ（ディレクトリ）といった階層で管理する。データ共有やデータの保存といった目的で使用される。**Amazon EFS**や**FSx**がこれにあたる。

**オブジェクトストレージ**は、ファイルに任意のメタデータを追加してオブジェクトとして管理するストレージ。ファイルストレージとは違い、フラットな構造で管理されるため、拡張性が高い。ファイルの内容をストレージ内で直接操作することはできず、作成済みのデータに対する、HTTP（HTTPS）経由の登録・削除・参照といった操作ができる。更新頻度の少ないデータや大容量のマルチメディアコンテンツを保存する用途で使われる。**Amazon S3**や**Amazon S3 Glacier**がこれにあたる。

|                      | ブロックストレージ                 | ファイルストレージ             | オブジェクトストレージ                     |
| -------------------- | ---------------------------------- | ------------------------------ | ------------------------------------------ |
| 管理単位             | ブロック                           | ファイル                       | オブジェクト                               |
| データライフサイクル | 追加・更新・削除                   | 追加・更新・削除               | 追加・削除                                 |
| プロトコル           | SATA、SCSI、FC                     | CIFS、NFS                      | HTTP（HTTPS）                              |
| メタデータ           | 固定情報のみ                       | 固定情報のみ                   | カスタマイズ可能                           |
| ユースケース         | データベース、トランザクションログ | ファイル共有、データアーカイブ | マルチメディアコンテンツ、データアーカイブ |


## データベースサービス

システムの構成要素としてなくてはならないデータベースは、大きく分けてRDBとNoSQLと呼ばれる2つのアーキテクチャに分類できる。

**RDB**（Relational Database）は、データを表（テーブル）形式で表現し、各テーブルの関係を定義・関連付けすることでデータを管理する。RDBの操作には**SQL**（Structured Query Language）を使用する。**Amazon RDS**と**Amazon Redshift**がこれにあたる。一般的なRDBMSソフトウェアとして、Oracle、Microsoft SQL Server、MySQL、PostgreSQLなどが挙げられる。

**NoSQL**（Not Only SQL）は、SQLを使わないデータベースアーキテクチャの総称。様々なデータモデルが存在し、柔軟でスキーマレスなデータモデル、水平スケーラビリティ、分散アーキテクチャ、高速な処理、などそれぞれに特徴がある。**Amazon DynamoDB**、**Amazon ElastiCache**、**Amazon Neptune**、**Amazon DocumentDB**、**Amazon Keyspaces**がこれにあたる。主なソフトウェアとして、Redis、Memcached（Key-Valueストア）、Cassandra、HBase（カラム指向データベース）、MongoDB、CouchDB（ドキュメント指向データベース）、Neo4j、Titan（グラフ指向データベース）などが挙げられる。


## セキュリティとアイデンティティ

### AWSアカウントの種類

**AWSアカウント**は、AWSへサインアップするときに作成されるアカウントで、**ルートユーザ**とも呼ばれる。

**IAMユーザ**は、AWSを利用する各利用者向けのアカウントであり、AWSアカウントでログインしてIAMユーザを作成する必要がある。

複数のAWSアカウントを管理するための**AWS Organizations**（組織アカウント）もあり、AWSサービスの請求を一括決済することが可能となっている。また、各アウントごとに利用できるサービスを制限する**サービスコントロールポリシー**（SCP）も利用できる。

### AWSアカウント

AWSアカウントはルートユーザとも呼ばれ、AWSの全サービスに対してネットワーク上のどこからでも操作できる権限を持つ。できる限りルートユーザは使わず、IAMユーザを利用する方がよい。また、AWSアカウントは**多要素認証**（Multi-Factor Authentication、MFA）によりセキュリティを強固にしておくようにするとよい。

### IAMポリシー

**IAMポリシー**は、**Action**（どのサービスの）、**Resource**（どういう機能や範囲を）、**Effect**（許可/拒否）という3つのルールに基づいて様々な権限を設定する。IAMでは、ユーザやグループ、ロールに付与する権限をオブジェクトとして管理することが可能で、これを**ポリシー**と呼ぶ。

**インラインポリシー**は、対象ごとに作成・付与するポリシーで複数のユーザ・グループに同種の権限を付与するには向いていない。

**管理ポリシー**は、1つのポリシーを複数のユーザやグループに適用できる。**AWS管理ポリシー**は、AWS側が用意しているポリシーで、管理者権限やPowerUser、サービスごとのポリシーなどがある。**カスタマー管理ポリシー**は、ユーザ自身が管理するポリシーで、インラインポリシーと同じように設定できる。

### IAMユーザとIAMグループ

ルートユーザはIAMユーザやグループに対して操作を制限することができる。IAMユーザの管理はセキュリティの要になるため、注意して権限を適切に制御する。

**ユーザ**とは、AWSを利用するために各利用者に1つずつ与えられる認証情報（ID）である。ユーザIDとパスワードを用いた認証は、Webコンソールにログインするときに使用する。アクセスキーとシークレットアクセスキーを用いた認証は、CLIやAPIからAWSのリソースにアクセスする場合に使用する。

**グループ**とは、同じ権限を持ったユーザの集まりのこと。グループは、グループ内のユーザの権限を管理することができる。

### IAMロール

**IAMロール**は、永続的な権限を保持するユーザとは異なり、一時的にAWSリソースへのアクセス権限を付与する場合に使用する。

- EC2インスタンス上で稼働するアプリケーションに一時的にAWSのリソースへアクセスする権限を与えたい場合
- 複数のAWSアカウント間のリソースを1つのIAMユーザで操作したい場合（**クロスアカウントアクセス**）
- 社内のAD（Active Directory）サーバに登録されているアカウントを使用してAWSリソースにアクセスしたい場合（**IDフェデレーション**）
- FacebookやGoogleアカウントを使用してAWSリソースにアクセスしたい場合（**Web ID フェデレーション**）

「アプリケーションに対してSESへの一時的なアクセス権限をEC2インスタンスから取得し、SESからメールを送信する」といったパターンがよく用いられている。


## アプリケーションサービス

AWSは、EC2やRDS、VPCといった[IaaS](../internet/01_basic_knowledge_of_network.md#クラウドの利用)や[PaaS](../internet/01_basic_knowledge_of_network.md#クラウドの利用)のみならず、[SaaS](../internet/01_basic_knowledge_of_network.md#クラウドの利用)と呼ばれるようなアプリケーションサービスも展開している。AWSのアプリケーションサービスは、AWSが提供するサーバリソースの上に構築されており、サーバとアプリケーションのメンテナンスはAWSが行う。


## デバロッパツール

アプリケーションは通常、リリース後も継続的な不具合調整や機能追加などを行っていく。そのため、ソースコードをビルドしたり、ユニットテストを走らせたりといった開発プロセスの自動化が重要となる。このような考え方は、**継続インテグレーション**（**CI**）や**継続的デリバリー**（**CD**）と呼ばれる。AWSは、Codeシリーズという**CI/CD環境**をマネージドサービスとして提供している。

### Codeシリーズ

- **CodeCommit**は、ソースコードを管理するGitリポジトリサービス。
- **CodeBuild**は、ソースコードのビルド/テスティングサービス。
- **CodeDeploy**は、ビルドされたモジュール（アーティファクト）のデプロイサービス。
- **CodePipeline**は、上記3つのサービスを束ねて、一連の開発プロセスを自動化するサービス。
- **CodeStar**は、上記4つのサービスを利用したCI/CD環境を自動構築するサービス。
