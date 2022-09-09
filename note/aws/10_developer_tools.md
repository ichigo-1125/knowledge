# デバロッパツール


## 目次

1. [CodeCommit](#codecommit)
1. [CodeBuild](#codebuild)
1. [CodeDeploy](#codedeploy)
1. [CodePipeline](#codepipeline)


## CodeCommit

**CodeCommit**は、ソースコード管理のためのGitリポジトリを提供するマネージドサービス。**Git**を用いたソースコードのバージョン管理は現在の開発のデファクトスタンダードで、CodeCommitはGitリポジトリを提供するSaaSのひとつである。

CodeCommitは、IAMユーザを利用して権限管理を行うことができる、他のAWSサービスとシームレスに連携できる、**プルリクエスト**機能がある、といった特徴がある。


## CodeBuild

**CodeBuild**は、ソースコードのコンパイル/ビルド環境を提供するマネージドサービス。

ビルド環境のランタイムとして、JavaやPHP、Python、Ruby、Node.jsなどを標準でサポートしており、個人で用意したDockerイメージを利用することもできる。

ビルドの定義は**buildspec.yml**に記載する。

また、料金が従量課金型である点もひとつの特徴である。


## CodeDeploy

**CodeDeploy**は、ビルド済みのモジュール（**アーティファクト**）をサーバへデプロイする工程を自動化するサービス。また、新しいモジュールに不具合が見つかったという場合に備えて、**ロールバック**の機能もある。

デプロイの定義は**appspec.yml**に定義する。また、デプロイ方式についても任意に決定することができる。


## CodePipeline

**CodePipeline**は、ソースコードが変更されてから検証環境にデプロイするまでの流れを自動化することができる。また、リリースの承認プロセスをパイプラインの途中に挟むことも可能で、チーム開発の権限管理にも適している。