# AWS


## AWSの基礎知識

- [ ] [AWS](./01_basic_knowledge_of_aws.md#aws)
	- [ ] [可用性](./01_basic_knowledge_of_aws.md#クラウド設計のポイント)
	- [ ] [スケーラビリティ](./01_basic_knowledge_of_aws.md#クラウド設計のポイント)
	- [ ] [パフォーマンス](./01_basic_knowledge_of_aws.md#クラウド設計のポイント)
	- [ ] [コスト効率](./01_basic_knowledge_of_aws.md#クラウド設計のポイント)
	- [ ] [セキュリティ](./01_basic_knowledge_of_aws.md#クラウド設計のポイント)
- [ ] [リージョン](./01_basic_knowledge_of_aws.md#リージョンとaz)
- [ ] [アベイラビリティゾーン（AZ）](./01_basic_knowledge_of_aws.md#リージョンとaz)
	- [ ] [データセンター](./01_basic_knowledge_of_aws.md#リージョンとaz)
- [ ] [マルチAZ](./01_basic_knowledge_of_aws.md#マルチaz)


## サービス概要

- [ ] [コンピューティングサービス](./02_overview_of_services.md#コンピューティングサービス)
- [ ] [運用支援サービス](./02_overview_of_services.md#運用支援サービス)
- [ ] [ストレージサービス](./02_overview_of_services.md#ストレージサービス)
	- [ ] [ブロックストレージ](./02_overview_of_services.md#ストレージサービス)
	- [ ] [ファイルストレージ](./02_overview_of_services.md#ストレージサービス)
	- [ ] [オブジェクトストレージ](./02_overview_of_services.md#ストレージサービス)
- [ ] [データベースサービス](./02_overview_of_services.md#データベースサービス)
	- [ ] [RDB](./02_overview_of_services.md#データベースサービス)
		- [ ] [SQL](./02_overview_of_services.md#データベースサービス)
	- [ ] [NoSQL](./02_overview_of_services.md#データベースサービス)
- [ ] [AWSアカウント](./02_overview_of_services.md#AWSアカウントの種類)
	- [ ] [ルートユーザ](./02_overview_of_services.md#AWSアカウント)
	- [ ] [IAMユーザ](./02_overview_of_services.md#iamユーザとiamグループ)
		- [ ] [IAMポリシー](./02_overview_of_services.md#iamポリシー)
			- [ ] [Action、Resource、Effect](./02_overview_of_services.md#iamポリシー)
			- [ ] [ポリシー](./02_overview_of_services.md#iamポリシー)
				- [ ] [インラインポリシー](./02_overview_of_services.md#iamポリシー)
				- [ ] [管理ポリシー](./02_overview_of_services.md#iamポリシー)
					- [ ] [AWS管理ポリシー](./02_overview_of_services.md#iamポリシー)
					- [ ] [カスタマー管理ポリシー](./02_overview_of_services.md#iamポリシー)
		- [ ] [IAMグループ](./02_overview_of_services.md#iamユーザとiamグループ)
	- [ ] [IAMロール](./02_overview_of_services.md#iamロール)
		- [ ] [クロスアカウントアクセス](./02_overview_of_services.md#iamロール)
		- [ ] [IDフェデレーション](./02_overview_of_services.md#iamロール)
		- [ ] [Web ID フェデレーション](./02_overview_of_services.md#iamロール)
	- [ ] [AWS Organizations](./02_overview_of_services.md#AWSアカウントの種類)
		- [ ] [サービスコントロールポリシー（SCP）](./02_overview_of_services.md#AWSアカウントの種類)
- [ ] [アプリケーションサービス](./02_overview_of_services.md#アプリケーションサービス)
- [ ] [デバロッパツール](./02_overview_of_services.md#デバロッパツール)
	- [ ] [継続インテグレーション（CI）](./02_overview_of_services.md#デバロッパツール)
	- [ ] [継続的デリバリー（CD）](./02_overview_of_services.md#デバロッパツール)
	- [ ] [CI/CD環境](./02_overview_of_services.md#デバロッパツール)
	- [ ] [Codeシリーズ](./02_overview_of_services.md#デバロッパツール)


## ネットワーキングとコンテンツ配信

- [ ] [VPC](./03_networking_and_content_delivery.md#vpc)
	- [ ] [サブネット](./03_networking_and_content_delivery.md#サブネット)
		- [ ] [パブリックサブネット](./03_networking_and_content_delivery.md#サブネット)
		- [ ] [プライベートサブネット](./03_networking_and_content_delivery.md#サブネット)
	- [ ] [セキュリティグループ](./03_networking_and_content_delivery.md#セキュリティグループ)
		- [ ] [インバウンド](./03_networking_and_content_delivery.md#セキュリティグループ)
		- [ ] [アウトバウンド](./03_networking_and_content_delivery.md#セキュリティグループ)
	- [ ] [ネットワークACL](./03_networking_and_content_delivery.md#ネットワークacl)
	- [ ] [ゲートウェイ](./03_networking_and_content_delivery.md#ゲートウェイ)
		- [ ] [インターネットゲートウェイ（IGW）](./03_networking_and_content_delivery.md#ゲートウェイ)
			- [ ] [単一障害点（SPOF）](./03_networking_and_content_delivery.md#ゲートウェイ)
		- [ ] [NATゲートウェイ](./03_networking_and_content_delivery.md#ゲートウェイ)
	- [ ] [仮想プライベートゲートウェイ（VPG）](./03_networking_and_content_delivery.md#ゲートウェイ)
	- [ ] [VPCエンドポイント](./03_networking_and_content_delivery.md#vpcエンドポイント)
	- [ ] [ゲートウェイエンドポイント](./03_networking_and_content_delivery.md#vpcエンドポイント)
	- [ ] [インタフェースゲートポイント](./03_networking_and_content_delivery.md#vpcエンドポイント)
		- [ ] [AWS PrivateLink](./03_networking_and_content_delivery.md#vpcエンドポイント)
	- [ ] [VPCピアリング](./03_networking_and_content_delivery.md#ピアリング接続)
		- [ ] [トランジット](./03_networking_and_content_delivery.md#ピアリング接続)
	- [ ] [VPCフローログ](./03_networking_and_content_delivery.md#vpcフローログ)
		- [ ] [ENI](./03_networking_and_content_delivery.md#vpcフローログ)

- [ ] [AWS Direct Connect](./03_networking_and_content_delivery.md#direct-connect)
	- [ ] [Direct Connect Gateway](./03_networking_and_content_delivery.md#direct-connect)
	- [ ] [AWS Transit Gateway](./03_networking_and_content_delivery.md#direct-connect)

- [ ] [Amazon CloudFront](./03_networking_and_content_delivery.md#cloudfront)
	- [ ] [バックエンドサーバ（オリジンサーバ）](./03_networking_and_content_delivery.md#cloudfront)
	- [ ] [CDN](./03_networking_and_content_delivery.md#cloudfront)
	- [ ] [エッジロケーション](./03_networking_and_content_delivery.md#cloudfront)
	- [ ] [レイテンシー](./03_networking_and_content_delivery.md#cloudfront)
	- [ ] [キャッシュルール](./03_networking_and_content_delivery.md#キャッシュルール)

- [ ] [Route53](./03_networking_and_content_delivery.md#route53)
	- [ ] [ゾーン情報](./03_networking_and_content_delivery.md#ドメイン管理)
	- [ ] [権威DNS](./03_networking_and_content_delivery.md#権威dns)
	- [ ] [キャッシュDNS](./03_networking_and_content_delivery.md#権威dns)
	- [ ] [ホストゾーン](./03_networking_and_content_delivery.md#ホストゾーンとレコード情報)
	- [ ] [レコード情報](./03_networking_and_content_delivery.md#ホストゾーンとレコード情報)
		- [ ] [Aレコード](./03_networking_and_content_delivery.md#ホストゾーンとレコード情報)
		- [ ] [MXレコード](./03_networking_and_content_delivery.md#ホストゾーンとレコード情報)
		- [ ] [CNAMEレコード](./03_networking_and_content_delivery.md#ホストゾーンとレコード情報)
		- [ ] [Aliasレコード](./03_networking_and_content_delivery.md#ホストゾーンとレコード情報)
			- [ ] [FADN](./03_networking_and_content_delivery.md#ホストゾーンとレコード情報)
			- [ ] [Zone Apex](./03_networking_and_content_delivery.md#ホストゾーンとレコード情報)
	- [ ] [トラフィックルーティング](./03_networking_and_content_delivery.md#トラフィックルーティング)
		- [ ] [シンプルルーティングポリシー](./03_networking_and_content_delivery.md#トラフィックルーティング)
		- [ ] [フェイルオーバールーティングポリシー](./03_networking_and_content_delivery.md#トラフィックルーティング)
			- [ ] [Sorryサーバ](./03_networking_and_content_delivery.md#トラフィックルーティング)
		- [ ] [位置情報ルーティングポリシー](./03_networking_and_content_delivery.md#トラフィックルーティング)
		- [ ] [地理的近接性ルーティングポリシー](./03_networking_and_content_delivery.md#トラフィックルーティング)
		- [ ] [レイテンシールーティングポリシー](./03_networking_and_content_delivery.md#トラフィックルーティング)
		- [ ] [複数値回答ルーティングポリシー](./03_networking_and_content_delivery.md#トラフィックルーティング)
		- [ ] [加重ルーティングポリシー](./03_networking_and_content_delivery.md#トラフィックルーティング)
	- [ ] [トラフィックフロー](./03_networking_and_content_delivery.md#トラフィックフロー)
	- [ ] [DNSフェイルオーバー](./03_networking_and_content_delivery.md#dnsフェイルオーバー)
		- [ ] [フォールトトレラントアーキテクチャ](./03_networking_and_content_delivery.md#dnsフェイルオーバー)


## コンピューティング

- [ ] [EC2](./04_computing.md#ec2)
	- [ ] [イメージ](./04_computing.md#ec2)
		- [ ] [AMI](./04_computing.md#ec2)
	- [ ] [インスタンスタイプ](./04_computing.md#ec2における性能)
		- [ ] [インスタンスファミリー](./04_computing.md#ec2における性能)
		- [ ] [世代](./04_computing.md#ec2における性能)
		- [ ] [インスタンスサイズ](./04_computing.md#ec2における性能)
		- [ ] [EBS最適化インスタンス](./04_computing.md#ec2における性能)
	- [ ] [オンデマンドインスタンス](./04_computing.md#スポットインスタンスとリザーブドインスタンス)
		- [ ] [従量課金型](./04_computing.md#ec2における費用)
		- [ ] [Running](./04_computing.md#ec2における費用)
		- [ ] [Stopped](./04_computing.md#ec2における費用)
		- [ ] [Terminated](./04_computing.md#ec2における費用)
	- [ ] [スポットインスタンス](./04_computing.md#スポットインスタンスとリザーブドインスタンス)
	- [ ] [リザーブドインスタンス](./04_computing.md#スポットインスタンスとリザーブドインスタンス)
	- [ ] [スケジュールされたリザーブドインスタンス](./04_computing.md#スポットインスタンスとリザーブドインスタンス)
	- [ ] [インスタンスの分類](./04_computing.md#インスタンスの分類と用途)
		- [ ] [汎用](./04_computing.md#インスタンスの分類と用途)
		- [ ] [コンピューティング最適化](./04_computing.md#インスタンスの分類と用途)
		- [ ] [メモリ最適化](./04_computing.md#インスタンスの分類と用途)
		- [ ] [高速コンピューティング](./04_computing.md#インスタンスの分類と用途)
		- [ ] [ストレージ最適化](./04_computing.md#インスタンスの分類と用途)
	- [ ] [Savings Plans](./04_computing.md#savings-plans)
		- [ ] [Compute Savings Plans](./04_computing.md#savings-plans)
	
- [ ] [ELB](./04_computing.md#elb)
	- [ ] [スケールアップ](./04_computing.md#スケールアップとスケールアウト)
	- [ ] [スケールアウト](./04_computing.md#スケールアップとスケールアウト)
	- [ ] [スケールイン](./04_computing.md#スケールアップとスケールアウト)
	- [ ] [CLB](./04_computing.md#elbの種類)
	- [ ] [ALB](./04_computing.md#elbの種類)
	- [ ] [NLB](./04_computing.md#elbの種類)
	- [ ] [スパイク](./04_computing.md#elbの種類)
	- [ ] [ヘルスチェック](./04_computing.md#elbの種類)
	- [ ] [ステートレス](./04_computing.md#ステートレス性の確保)
	
- [ ] [Auto Scaling](./04_computing.md#auto-scaling)
	- [ ] [スケーリングポリシー](./04_computing.md#スケーリングポリシー)
		- [ ] [簡易スケーリング](./04_computing.md#スケーリングポリシー)
		- [ ] [ステップスケーリング](./04_computing.md#スケーリングポリシー)
		- [ ] [ターゲット追跡スケーリング](./04_computing.md#スケーリングポリシー)
	- [ ] [猶予期間](./04_computing.md#猶予期間)
	- [ ] [スケーリングクールダウン](./04_computing.md#ウォームアップとクールダウン)
	- [ ] [ウォームアップ](./04_computing.md#ウォームアップとクールダウン)
	- [ ] [ライフサイクルフック](./04_computing.md#ライフサイクルフック)
	- [ ] [終了ポリシー](./04_computing.md#終了ポリシー)
	
- [ ] [ECS](./04_computing.md#ecs)
	- [ ] [Docker](./04_computing.md#ecs)
		- [ ] [Task](./04_computing.md#ecs)
		- [ ] [Cluster](./04_computing.md#ecs)
		- [ ] [Task Definition](./04_computing.md#ecs)
		- [ ] [Service](./04_computing.md#ecs)
	- [ ] [AWS Fargate](./04_computing.md#その他のコンテナサービス)
	- [ ] [Kubernetes](./04_computing.md#その他のコンテナサービス)
		- [ ] [EKS](./04_computing.md#その他のコンテナサービス)
	- [ ] [ECR](./04_computing.md#その他のコンテナサービス)
	
- [ ] [Lambda](./04_computing.md#lambda)
	- [ ] [プロビジョニング](./04_computing.md#lambda)
	- [ ] [サーバレスアーキテクチャ](./04_computing.md#lambda)
	- [ ] [Lambda関数](./04_computing.md#lambda)
	- [ ] [キック](./04_computing.md#lambda)


## マネジメントとガバナンス

- [ ] [Amazon CloudWatch](./05_management_and_governance.md#cloudwatch)
	- [ ] [CloudWatch](./05_management_and_governance.md#cloudwatch)
	- [ ] [メトリクス](./05_management_and_governance.md#cloudwatch)
		- [ ] [標準メトリクス](./05_management_and_governance.md#cloudwatch)
		- [ ] [カスタムメトリクス](./05_management_and_governance.md#cloudwatch)
	- [ ] [CloudWatch Logs](./05_management_and_governance.md#cloudwatch-logs)
	- [ ] [CloudWatch Events](./05_management_and_governance.md#cloudwatch-events)
		- [ ] [イベントソース](./05_management_and_governance.md#cloudwatch-events)
			- [ ] [スケジュール](./05_management_and_governance.md#cloudwatch-events)
			- [ ] [イベント](./05_management_and_governance.md#cloudwatch-events)
		- [ ] [ターゲット](./05_management_and_governance.md#cloudwatch-events)
		- [ ] [EventBridge](./05_management_and_governance.md#cloudwatch-events)
	
- [ ] [AWS CloudTrail](./05_management_and_governance.md#cloudtrail)
	- [ ] [管理イベント](./05_management_and_governance.md#イベントの種類)
	- [ ] [データイベント](./05_management_and_governance.md#イベントの種類)


## ストレージ

- [ ] [EBS](./06_storage.md#ebs)
	- [ ] [ベースライン性能](./06_storage.md#ボリュームタイプ)
		- [ ] [ボリュームタイプ](./06_storage.md#ボリュームタイプ)
		- [ ] [マグネティックタイプ](./06_storage.md#ボリュームタイプ)
		- [ ] [汎用SSD](./06_storage.md#ボリュームタイプ)
			- [ ] [IOPS](./06_storage.md#ボリュームタイプ)
			- [ ] [バースト機能](./06_storage.md#ボリュームタイプ)
		- [ ] [プロビジョンドIOPS SSD](./06_storage.md#ボリュームタイプ)
		- [ ] [スループット最適化HDD](./06_storage.md#ボリュームタイプ)
			- [ ] [スループット](./06_storage.md#ボリュームタイプ)
		- [ ] [Cold HDD](./06_storage.md#ボリュームタイプ)
			- [ ] [シーケンシャルアクセス](./06_storage.md#ボリュームタイプ)
			- [ ] [ランダムアクセス](./06_storage.md#ボリュームタイプ)
	- [ ] [バースト性能](./06_storage.md#バースト性能)
	- [ ] [スナップショット機能](./06_storage.md#ebsの拡張と可用性とセキュリティ)
	- [ ] [EBSマルチアタッチ](./06_storage.md#ebsマルチアタッチ)

- [ ] [EFS](./06_storage.md#efs)
	- [ ] [NFS](./06_storage.md#efs)
	- [ ] [amazon-efs-utils](./06_storage.md#efs)
	- [ ] [分散ファイルシステム](./06_storage.md#efsの構成要素)
	- [ ] [マウントターゲット](./06_storage.md#efsの構成要素)
		- [ ] [ターゲットポイント](./06_storage.md#efsの構成要素)
	- [ ] [パフォーマンスモード](./06_storage.md#パフォーマンスモード)
		- [ ] [汎用パフォーマンスモード](./06_storage.md#パフォーマンスモード)
		- [ ] [最大I/Oパフォーマンスモード](./06_storage.md#パフォーマンスモード)
		- [ ] [PercentIOLimit](./06_storage.md#パフォーマンスモード)
	- [ ] [スループットモード](./06_storage.md#スループットモード)
		- [ ] [バーストスループットモード](./06_storage.md#スループットモード)
		- [ ] [プロビジョニングバーストスループットモード](./06_storage.md#スループットモード)
		- [ ] [BurstCreditBalance](./06_storage.md#スループットモード)

- [ ] [S3](./06_storage.md#s3)
	- [ ] [バケット](./06_storage.md#s3の構成要素)
	- [ ] [オブジェクト](./06_storage.md#s3の構成要素)
	- [ ] [メタデータ](./06_storage.md#s3の構成要素)
	- [ ] [結果整合性方式](./06_storage.md#s3の耐久性と整合性)
	- [ ] [ストレージクラス](./06_storage.md#ストレージクラス)
		- [ ] [SLA](./06_storage.md#ストレージクラス)
		- [ ] [S3標準](./06_storage.md#ストレージクラス)
		- [ ] [S3標準 - 低頻度アクセス](./06_storage.md#ストレージクラス)
		- [ ] [S3 1ゾーン - IA](./06_storage.md#ストレージクラス)
		- [ ] [S3 Intelligent - Tiering](./06_storage.md#ストレージクラス)
		- [ ] [S3 Glacier](./06_storage.md#ストレージクラス)
		- [ ] [S3 Glacier Deep Archive](./06_storage.md#ストレージクラス)
	- [ ] [ライフサイクル管理](./06_storage.md#ライフサイクル管理)
		- [ ] [ライフサイクル](./06_storage.md#ライフサイクル管理)
		- [ ] [移行アクション](./06_storage.md#ライフサイクル管理)
		- [ ] [有効期限アクション](./06_storage.md#ライフサイクル管理)
	- [ ] [バージョニング機能](./06_storage.md#バージョニング機能)
	- [ ] [Webサイトホスティング機能](./06_storage.md#webサイトホスティング機能)
	- [ ] [バケットポリシー](./06_storage.md#s3のアクセス管理)
	- [ ] [署名付きURL](./06_storage.md#署名付きurl)
	- [ ] [データ暗号化](./06_storage.md#データ暗号化)
		- [ ] [サーバ側での暗号化](./06_storage.md#データ暗号化)
		- [ ] [クライアント側での暗号化](./06_storage.md#データ暗号化)
	- [ ] [ブロックパブリックアクセス機能](./06_storage.md#ブロックパブリックアクセス機能)
	- [ ] [S3 Access Analyzer](./06_storage.md#ブロックパブリックアクセス機能)
	- [ ] [S3 Select](./06_storage.md#s3のその他の機能)
	- [ ] [S3 Transfer Acceleratioin](./06_storage.md#s3のその他の機能)

- [ ] [S3 Glacier](./06_storage.md#s3-glacier)
	- [ ] [ボールト](./06_storage.md#s3-glacierの構成要素)
	- [ ] [アーカイブ](./06_storage.md#s3-glacierの構成要素)
	- [ ] [インベントリ](./06_storage.md#s3-glacierの構成要素)
		- [ ] [ListVaults API](./06_storage.md#s3-glacierの構成要素)
	- [ ] [ジョブ](./06_storage.md#s3-glacierの構成要素)
	- [ ] [高速](./06_storage.md#データの取り出しオプション)
	- [ ] [標準](./06_storage.md#データの取り出しオプション)
	- [ ] [バルク](./06_storage.md#データの取り出しオプション)
	- [ ] [S3 Glacier Select](./06_storage.md#s3-glaicier-select)
	- [ ] [削除禁止機能（ボールトロック）](./06_storage.md#削除禁止機能)

- [ ] [Storage Gateway](./06_storage.md#storage-gateway)
	- [ ] [ファイルゲートウェイ](./06_storage.md#ファイルゲートウェイ)
	- [ ] [ボリュームゲートウェイ](./06_storage.md#ボリュームゲートウェイ)
		- [ ] [キャッシュ型ボリューム](./06_storage.md#ボリュームゲートウェイ)
			- [ ] [プライマリストレージ](./06_storage.md#ボリュームゲートウェイ)
			- [ ] [キャッシュボリューム](./06_storage.md#ボリュームゲートウェイ)
			- [ ] [アップロードバッファボリューム](./06_storage.md#ボリュームゲートウェイ)
		- [ ] [保管型ボリューム](./06_storage.md#ボリュームゲートウェイ)
	- [ ] [テープゲートウェイ](./06_storage.md#テープゲートウェイ)
	- [ ] [CHAP認証](./06_storage.md#storage-gatewayのセキュリティ)
	
- [ ] [FSx](./06_storage.md#fsx)
	- [ ] [FSx for Windowsファイルサーバ](./06_storage.md#fsx-for-windowsファイルサーバ)
	- [ ] [FSx for Lustre](./06_storage.md#fsx-for-lustre)


## データベース

- [ ] [RDS](./07_database.md#rds)
	- [ ] [マルチAZ構成](./07_database.md#マルチaz構成)
	- [ ] [フェイルオーバ](./07_database.md#マルチaz構成)
	- [ ] [リードレプリカ](./07_database.md#リードレプリカ)
		- [ ] [非同期レプリケーション](./07_database.md#リードレプリカ)
	- [ ] [自動バックアップ](./07_database.md#バックアップとリストア)
	- [ ] [手動スナップショット](./07_database.md#バックアップとリストア)
	- [ ] [データのリストア](./07_database.md#バックアップとリストア)
	- [ ] [ポイントインタイムリカバリ](./07_database.md#バックアップとリストア)
	- [ ] [Amazon Aurora](./07_database.md#aurora)
		- [ ] [DBクラスタ](./07_database.md#aurora)
		- [ ] [クラスタボリューム](./07_database.md#aurora)
		- [ ] [Auroraレプリカ](./07_database.md#aurora)
		- [ ] [クラスタエンドポイント](./07_database.md#aurora)
		- [ ] [読み取りエンドポイント](./07_database.md#aurora)
		- [ ] [インスタンスエンドポイント](./07_database.md#aurora)
		- [ ] [カスタムエンドポイント](./07_database.md#aurora)
	
- [ ] [Redshift](./07_database.md#redshift)
	- [ ] [データウェアハウス](./07_database.md#redshift)
	- [ ] [Redshiftクラスタ](./07_database.md#redshiftの構成)
		- [ ] [リーダノード](./07_database.md#redshiftの構成)
		- [ ] [コンピュートノード](./07_database.md#redshiftの構成)
		- [ ] [ノードスライス](./07_database.md#redshiftの構成)
			- [ ] [スライス](./07_database.md#redshiftの構成)
	- [ ] [列指向型（カラムナ）データベース](./07_database.md#redshiftの構成)
	- [ ] [ゾーンマップ](./07_database.md#ゾーンマップ)
	- [ ] [MPP](./07_database.md#redshiftの拡張性)
	- [ ] [シェアードナッシング](./07_database.md#redshiftの拡張性)
	- [ ] [wlm_json_configuration](./07_database.md#ワークロードの管理機能)
	- [ ] [Redshift Spectrum](./07_database.md#redshift-spectrum)
	
- [ ] [DynamoDB](./07_database.md#dynamodb)
	- [ ] [Key-Value型データベース](./07_database.md#dynamodb)
	- [ ] [トランザクション](./07_database.md#dynamodb)
	- [ ] [スループットキャパシティ](./07_database.md#スループットキャパシティ)
		- [ ] [Read Capacity Unit](./07_database.md#スループットキャパシティ)
		- [ ] [Write Capacity Unit](./07_database.md#スループットキャパシティ)
	- [ ] [データパーティショニング](./07_database.md#データパーティショニング)
	- [ ] [プライマリキー](./07_database.md#プライマリキーとインデックス)
		- [ ] [パーティションキー](./07_database.md#プライマリキーとインデックス)
		- [ ] [複合キーテーブル](./07_database.md#プライマリキーとインデックス)
		- [ ] [インデックス](./07_database.md#プライマリキーとインデックス)
			- [ ] [セカンダリインデックス](./07_database.md#プライマリキーとインデックス)
			- [ ] [ローカルセカンダリインデックス](./07_database.md#プライマリキーとインデックス)
			- [ ] [グローバルセカンダリインデックス](./07_database.md#プライマリキーとインデックス)
	- [ ] [TTL](./07_database.md#ttl)
	- [ ] [DynamoDB Streams](./07_database.md#dynamodb-streams)
	- [ ] [Consistent Read](./07_database.md#consistent-read)
	- [ ] [DynamoDB Accelerator（DAX）](./07_database.md#dynamodb-accelerator)

- [ ] [ElastiCache](./07_database.md#elasticache)
	- [ ] [Mmemcached](./07_database.md#elasticache)
		- [ ] [ノードエンドポイント](./07_database.md#memcached版elesticache)
		- [ ] [設定エンドポイント](./07_database.md#memcached版elesticache)
	- [ ] [Redis](./07_database.md#elasticache)
		- [ ] [クラスタモード](./07_database.md#redis版elasticache)
			- [ ] [シャード](./07_database.md#redis版elasticache)
		- [ ] [ノードエンドポイント](./07_database.md#redis版elasticache)
		- [ ] [プライマリエンドポイント](./07_database.md#redis版elasticache)
		- [ ] [設定エンドポイント](./07_database.md#redis版elasticache)

- [ ] [Amazon Neptune](./07_database.md#amazon-neptune)
	- [ ] [グラフデータベース](./07_database.md#amazon-neptune)

- [ ] [Amazon DocumentDB](./07_database.md#amazon-documentdb)
	- [ ] [MongoDB](./07_database.md#amazon-documentdb)
	- [ ] [ドキュメントデータベース](./07_database.md#amazon-documentdb)

- [ ] [Amazon Keyspaces](./07_database.md#amazon-keyspaces)
	- [ ] [Apache Cassandra](./07_database.md#amazon-keyspaces)
	- [ ] [列指向データ、行指向データ](./07_database.md#amazon-keyspaces)

- [ ] [Amazon Timestream](./07_database.md#amazon-timestream)
	- [ ] [時系列データベース](./07_database.md#amazon-timestream)
	- [ ] [時系列データ](./07_database.md#amazon-timestream)

- [ ] [Amazon QLDB](./07_database.md#amazon-qldb)
	- [ ] [台帳データベース](./07_database.md#amazon-qldb)


## セキュリティとアイデンティティ

- [ ] [KMS](./08_security_and_identity.md#kmsとcloudhsm)
	- [ ] [Encrypt](./08_security_and_identity.md#kmsの機能)
	- [ ] [Decrypt](./08_security_and_identity.md#kmsの機能)
	- [ ] [GenerateDataKey](./08_security_and_identity.md#kmsの機能)
	- [ ] [マスタキー（CMK）](./08_security_and_identity.md#マスタキーとデータキー)
	- [ ] [データキー（CDK）](./08_security_and_identity.md#マスタキーとデータキー)
	- [ ] [エンベロープ暗号化](./08_security_and_identity.md#マスタキーとデータキー)

- [ ] [CloudHSM](./08_security_and_identity.md#kmsとcloudhsm)

- [ ] [ACM](./08_security_and_identity.md#acm)
	- [ ] [サーバ証明書](./08_security_and_identity.md#証明書の役割と実体)
	- [ ] [SSL/TLS](./08_security_and_identity.md#証明書の役割と実体)
		- [ ] [SSL証明書](./08_security_and_identity.md#証明書の役割と実体)
	- [ ] [認証局（CA）](./08_security_and_identity.md#証明書の役割と実体)
	- [ ] [自己証明書](./08_security_and_identity.md#証明書の役割と実体)
	- [ ] [ドメイン証明](./08_security_and_identity.md#証明書の役割と実体)
	- [ ] [組織認証](./08_security_and_identity.md#証明書の役割と実体)
	- [ ] [拡張認証](./08_security_and_identity.md#証明書の役割と実体)


## アプリケーションサービス

- [ ] [SQS](./09_application_integration.md#sqs)
	- [ ] [キュー](./09_application_integration.md#sqs)
	- [ ] [Standardキュー](./09_application_integration.md#standardキューとfifoキュー)
	- [ ] [FIFOキュー](./09_application_integration.md#standardキューとfifoキュー)
	- [ ] [ロングポーリング](./09_application_integration.md#ロングポーリング)
	- [ ] [ショートポーリング](./09_application_integration.md#ロングポーリング)
	- [ ] [可視性タイムアウト](./09_application_integration.md#可視性タイムアウト)
	- [ ] [遅延キュー](./09_application_integration.md#遅延キューとメッセージタイマー)
	- [ ] [メッセージタイマー](./09_application_integration.md#遅延キューとメッセージタイマー)
	- [ ] [デッドレターキュー](./09_application_integration.md#デッドレターキュー)

- [ ] [SWF](./09_application_integration.md#awsのワークフローサービス)
- [ ] [Amazon Step Functions](./09_application_integration.md#awsのワークフローサービス)

- [ ] [SNS](./09_application_integration.md#sns)
	- [ ] [トピック](./09_application_integration.md#トピックと講読)
	- [ ] [購読](./09_application_integration.md#トピックと講読)
		- [ ] [Publisher](./09_application_integration.md#トピックと講読)
		- [ ] [Subscriber](./09_application_integration.md#トピックと講読)
	
- [ ] [SES](./09_application_integration.md#ses)
	- [ ] [SPF](./09_application_integration.md#ses)
	- [ ] [DKIM](./09_application_integration.md#ses)


## デバロッパツール

- [ ] [CodeCommit](./10_developer_tools.md#codecommit)
	- [ ] [Git](./10_developer_tools.md#codecommit)
	- [ ] [プルリクエスト](./10_developer_tools.md#codecommit)
	
- [ ] [CodeBuild](./10_developer_tools.md#codebuild)
	- [ ] [buildspec.yml](./10_developer_tools.md#codebuild)
	
- [ ] [CodeDeploy](./10_developer_tools.md#codedeploy)
	- [ ] [appspec.yml](./10_developer_tools.md#codedeploy)
	
- [ ] [Code Pipeline](./10_developer_tools.md#codedeploy)


## プロビジョニングサービス

- [ ] [Elastic Beanstalk](./11_provisioning.md#elastic-beanstalk)
	- [ ] [Webサーバ構成](./11_provisioning.md#elastic-beanstalk)
	- [ ] [Batchワーカ構成](./11_provisioning.md#elastic-beanstalk)
	- [ ] [AWS Toolkit for Eclipse](./11_provisioning.md#elastic-beanstalkの利用方法)
	- [ ] [AWS CLI](./11_provisioning.md#elastic-beanstalkの利用方法)
	- [ ] [EB CLI](./11_provisioning.md#elastic-beanstalkの利用方法)

- [ ] [OpsWorks](./11_provisioning.md#opsworks)
	- [ ] [Chef](./11_provisioning.md#opsworks)
	- [ ] [レシピ](./11_provisioning.md#opsworks)
	- [ ] [Chef Clientローカル方式](./11_provisioning.md#opsworks)
	- [ ] [Chef Server/Client方式](./11_provisioning.md#opsworks)
	- [ ] [OpsWorksスタック](./11_provisioning.md#opsworksスタック)
		- [ ] [スタック](./11_provisioning.md#opsworksスタック)
		- [ ] [レイヤ](./11_provisioning.md#opsworksスタック)
	- [ ] [OpsWorksエージェント](./11_provisioning.md#opsworksスタック)
	- [ ] [Chef Automate](./11_provisioning.md#opsworks-for-chef-automate)

- [ ] [CloudFormation](./11_provisioning.md#opsworks-for-chef-automate)
	- [ ] [スタック](./11_provisioning.md#opsworks-for-chef-automate)
	- [ ] [テンプレート](./11_provisioning.md#opsworks-for-chef-automate)
		- [ ] [Resourcesセクション](./11_provisioning.md#cloudformationテンプレート)
		- [ ] [Parametersセクション](./11_provisioning.md#cloudformationテンプレート)
		- [ ] [Mappingsセクション](./11_provisioning.md#cloudformationテンプレート)
		- [ ] [擬似パラメータ](./11_provisioning.md#cloudformationテンプレート)
		- [ ] [組み込み関数](./11_provisioning.md#cloudformationテンプレート)
		- [ ] [Ref関数](./11_provisioning.md#cloudformationテンプレート)
		- [ ] [FindMap関数](./11_provisioning.md#cloudformationテンプレート)
		- [ ] [Select関数](./11_provisioning.md#cloudformationテンプレート)
		- [ ] [ImportValue関数](./11_provisioning.md#cloudformationテンプレート)


## 分析サービス

- [ ] [EMR](./12_analytics.md#emr)
	- [ ] [マスタノード](./12_analytics.md#emr)
	- [ ] [コアノード](./12_analytics.md#emr)
		- [ ] [HDFS](./12_analytics.md#emr)
	- [ ] [タスクノード](./12_analytics.md#emr)
	- [ ] [分散処理基盤](./12_analytics.md#分散処理基盤としてのemr)
	- [ ] [サポートアプリケーション](./12_analytics.md#分散処理アプリケーション基盤としてのemr)
	- [ ] [カスタムアプリケーション](./12_analytics.md#分散処理アプリケーション基盤としてのemr)
	
- [ ] [ETLツール](./12_analytics.md#etlツール)
	- [ ] [Kinesis](./12_analytics.md#kinesis)
		- [ ] [Data Stream](./12_analytics.md#kinesis)
		- [ ] [Data Firehose](./12_analytics.md#kinesis)
		- [ ] [Video Streams](./12_analytics.md#kinesis)
		- [ ] [Data Analytics](./12_analytics.md#kinesis)
	- [ ] [Data Pipeline](./12_analytics.md#data-pipeline)
	- [ ] [Glue](./12_analytics.md#glue)
		- [ ] [クローラ機能](./12_analytics.md#glue)
		- [ ] [データカタログ機能](./12_analytics.md#glue)
		- [ ] [ジョブ](./12_analytics.md#glue)

- [ ] [Amazon Athena](./12_analytics.md#amazon-athena)
- [ ] [Amazon QuickSight](./12_analytics.md#amazon-quicksight)