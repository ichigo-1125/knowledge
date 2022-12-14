# マネジメントとガバナンス


## 目次

1. [CloudWatch](#cloudwatch)
	1. [CloudWatch Logs](#cloudwatch-logs)
	1. [CloudWatch Events](#cloudwatch-events)
1. [CloudTrail](#cloudtrail)
	1. [イベントの種類](#イベントの種類)


## CloudWatch

**Amazon CloudWatch**は、運用監視を支援するマネージドサービスであり、システムの安定運用をサポートする。

メインの機能である**CloudWatch**は、各AWSリソースの状態（**メトリクス**）を定期的に取得するサービスである。AWSがあらかじめ定義している**標準メトリクス**と、利用者が独自に定義することができる**カスタムメトリクス**がある。CloudWatchではこれらのメトリクスを用いてアラートを定義することができる。

### CloudWatch Logs

**CloudWatch Logs**は、アプリケーションログやApacheログなどのログをモニタリングするサービス。エージェントを介してログを収集し、アラームを設定することもできる。

### CloudWatch Events

**CloudWatch Events**は、独自のトリガーと何かしらの後続アクションとの組み合わせを定義するサービス。独自のトリガーを**イベントソース**と呼び、後続アクションを**ターゲット**と呼ぶ。イベントソースにはスケジュールとイベントがある。**スケジュール**は期間・時間ベースをトリガーとし、**イベント**はAWSリソースの状態変化をトリガーにする。

CloudWatch Eventsは**EventBridge**に統合予定である。


## CloudTrail

**AWS CloudTrail**は、AWSに関する操作ログを自動的に取得するサービス。誰が、いつ、どのような操作をしたか、といった監査ログを残すことができる。

CloudWatch Logsと連携することで、事前に不正な操作を登録しておき、そのような操作が行われたときに通知するように設定することもできる。

### イベントの種類

**管理イベント**には、マネジメントコンソールへのログインやEC2インスタンスの作成、S3バケットの作成などがある。

**データイベント**には、S3バケット上のデータの操作、Lambda関数の実行などがある。

管理イベントの取得はデフォルトで有効であるが、データイベントの取得はデフォルトで無効となっているので注意。
