# 職務経歴書

-----

## 基本情報

|key|value|
|---|-----|
|名前| 穴澤 伸太郎 (旧姓 池田) |
|生年| 1991年 |
|居住地| 東京都杉並区 |
|最終学歴| 慶應義塾大学大学院 理工学部 情報工学科 |

-----

## 各種アカウント

|key|value|
|---|-----|
|GitHub|[momotaro98](https://github.com/momotaro98)|
|Qiita|[momotaro98](https://qiita.com/momotaro98)|
|Twitter|[@momotaro98_](https://twitter.com/momotaro98_)|
|Speaker Deck|[momotaro98](https://speakerdeck.com/momotaro98)|

-----

## 自己PR

- システムプロダクト開発にて要件定義、設計、開発、構築、運用を過去2つの職歴とも経験している
- 英語を使った業務経験を過去2つの職歴とも経験している
- Qiita、技術ブロクへ継続的に技術に関する記事を投稿している
- OSSへのコントリビュートを継続的に行っている
- 組織文化、開発者体験、リーン、アジャイルといったエンジニアリングマネジメントへの関心が高い

-----

## スキル

### 技術スタック

|名前| 実務で利用した期間 |備考|
|---|-----|---|
|Go| 4年 | WebApp, CLI, Library |
|JavaScript| 2年 | Node.js/jQuery |
|TypeScript| 1年 | AWS CDK |
|Python| 2年 | Flask |
|MySQL| 3年 | |
|SQLServer| 2年 | |
|Redis| 3年 | Cluster on AWS ElastiCache |
|Elasticsearch| 3年 | Cluster on AWS OpenSearch |
|AWS| 3年 | CloudWatch/SNS/IAM/CloudFormation/CodePipeline/Deploy/Build/Route53/S3/API Gateway/Lambda/ALB/ECS Fargate/Aurora DB/SQS/OpenSearch/DynamoDB/ElastiCache/Batch/Beanstalk/Kinesis |
|Azure| 1年 | Azure Functions/Table Strage/Queue Strage/Cosmos DB |
|Firebase| 1年 | Auth/Strage/Site |
|Terraform| 1年 | |
|Ansible| 1年 | |

### ツール、その他
  - CI/CD (TeamCity/Jenkins/CircleCI/GitLabCI/GitHub Actions)
  - Ticket management (JIRA/Trello/Backlog)
  - Document management (Confluence/GoogleDoc/Notion)

-----

## 今後やっていきたいロール / 伸ばしたいスキル

* SRE / DevOps エンジニア
  * [Four Keys](https://cloud.google.com/blog/products/devops-sre/using-the-four-keys-to-measure-your-devops-performance)などのビジネス貢献に関わる指標の可視化と開発チームへの改善仕組み提供
  * プロダクトの非機能品質（パフォーマンス、セキュリティ、可用性、等）の向上への貢献
* エンジニアリングマネージャー
  * 開発者体験の向上プロセスの設計・作成
  * Lean開発・フロー効率性を向上させるための組織設計、仕組みづくり
  * 優れたチームを築き上げるためのコーチング、採用

-----

## 職務経歴詳細

### 株式会社レアジョブ（現職）: 2019/11 ~

#### 概要

社内でプラットフォームと呼ばれるビジネスサービス基盤を担当するチームにて、バックエンド兼DevOpsエンジニアとして開発・運用をしていました。 また、フィリピンに在籍するエンジニアチームと英語を使ったコミュニケーションをメンバーの中で一番多く担っていました。

#### 詳細

**検索サービスリプレース開発・運用**

既存で存在していたモノリシックシステムに対する「他機能に影響を与えていた検索による既存MySQL DBへの負荷を取り除く」,「変更・リリース容易性を得る」,「レッスン・講師検索機能における業務仕様を明確化する」という課題が存在していました。その解決のため、新規にマイクロサービスとして検索サービスAPIを切り出すことを設計、実装、構築、運用すべてに責任を持ち目的を達成できました。
全社的な大きなリプレースプロジェクトであったため、設計からリリースまでに1年3ヶ月かけて実施しました。
レアジョブ英会話における検索サービスは複雑な既存仕様を持つレッスンドメイン、講師ドメイン、生徒ドメイン、と3つのドメインが交わるサービスであり様々な社内のチームと強調し仕様を整理しながら進めました。
検索サービスAPIのデータベースにはElasticsearchとRedisを採用、実装にはGo言語を採用しました。
技術的な課題として以下などがありひとつひとつ解決していきました。
* レッスン検索と講師検索というビジネス要件のためにElasticsearchでのデータスキーマをどのように持つか
* どのように過去のレッスンが検索対象とならないようにするか
* ElasticsearchのインデックスのMapping変更をどのように実現するか

- **利用した技術スタック**
  - Go、SAM、Lambda、Redis(ElastiCache)、Elasticsearch(OpenSearch)、SQS、MySQL(RDS AuroraDB)、API Gateway、VPC Endpoint、GitLab CI

**レッスン基盤サービスAPI開発**

レアジョブ社のサービスにて共通で存在するレッスン・カウンセリングの予約管理共通基盤サービスの開発・運用を担当していました。
以下のような改善タスクを提案し実施しました。
* 既存機能の要件定義とDBスキーマ変更
* 既存インフラからインフラコード（CloudFormation)を使ったインフラへの変更対応
* 負荷試験を新規に仕組み化し実施
* CICDを既存の複雑な状態のものからAWS CodePipeline、CodeDeployを利用

- **利用した技術スタック**
  - Go、ECS(Fargate)、ALB、MySQL(RDS AuroraDB)、API Gateway、GitLab CI、CodePipeline、CodeDeploy、CloudFormation

**レッスンデータの新規システムへのマイグレーションとデータ同期**

既存で存在していたモノリシックシステムにおけるレッスンデータを予約管理共通基盤サービスへと移行させる全社的な取り組みに共通基盤チームメンバーとして参画しました。全体のロードマップとしてまずは過去データを移行させ旧システムと共通基盤サービスにてリアルタイムのデータ同期を実現するシステムを設計・実装・構築・運用までチームの一員として担当しました。初期には複雑な業務仕様をヒアリングやドキュメント、コード参照によって調査し現在の業務において本当に必要な要素を洗い出しました。データ移行では既存の多量なデータを効率的に移行させる技術的方法をチームで検討し、データのリアルタイム同期の仕組みとしてデータ間の一貫性を保つための技術的課題解決に取り組みました。

- **利用した技術スタック**
  - Go、MySQL(RDS AuroraDB)、SQS、AWS Beanstalk

**決済基盤サービス/決済系バックオフィスツール開発**

新規に作成された全社的な決済共通基盤サービスの開発に携わりました。返金対応などのユーザーの決済に関わるバックオフィス業務用ツールの新規開発に対応するための機能の拡張を担当しました。また、このタスクに関連し共通基盤サービスとして既存にある認証認可システムにおいてバックオフィスツールを利用する社内ユーザーのみが利用できるように機能を設計、実装担当しました。開発にあたり、社内で利用している決済代行サービスのシステム仕様をドキュメントを読み込むことで把握し既存の不具合などの修正も実施しました。

- **利用した技術スタック**
  - 「レッスン基盤サービスAPI開発」と同様

-----

### 楽天グループ株式会社: 2017/04 ~ 2019/10

物流システム開発部署に所属し、Order Management System(OMS)と呼ばれるECサイト店舗向けの受注管理システムの開発と運用を担当していました。

受注業務のアプリケーションをメインにシステム設計・開発を担っていました。C#, .NET, Windows Serverのプロダクトになります。

* アジャイル開発の中ではスクラムマスタ兼務でプロジェクトに貢献
* CI/CDの改善や運用システムをAzureを利用し開発することを担当
* 運用面では受注業務だけでなく商品管理業務、在庫管理業務などの機能面も把握しカスタマー対応や障害対応を経験
* 日本語が不得意なエンジニアメンバーと英語を使ったコミュニケーションを継続
* プロパー社員としてプロジェクトとパートナースタッフのタスクマネジメント業務を経験

**より詳細な職務内容は以下のブログ記事を参照ください**

https://ochataro.hateblo.jp/entry/2019/10/31/152634

-----

### 副業

- "Mixlunch"と名付けたランチメートのマッチングサービスの開発とローンチ
  - Mixlunchは新卒楽天期の同期と起業を目標に作ったサービスです。ローンチまでは達成しましたが集客ができずビジネスモデルを再検討後マネタイズ設計が曖昧とわかりサービス継続を断念しました
  - サービスLPページ https://www.mixlunch.com/
  - GitHub URL 
    - バックエンドAPI (Go): https://github.com/momotaro98/mixlunch-service-apis
    - BFF API (Node.js): https://github.com/momotaro98/mixlunch-bff-apis
  - その他
    - ランチメイトのマッチングバッチはPythonで機械学習モデル利用を想定し実装しました。(ソースコードは非公開）

-----

### 大学・大学院での研究 2014/04 ~ 2017/03

#### [研究内容2] 機械学習モデルを利用した快適度フィードバックからの空調機の自動制御システムの研究

家庭内の空調機制御における省エネと快適さの両立を目指す最適化アルゴリズムの研究をしていました。
研究の中ではIoTデバイスを用いて実際の家庭に協力いただき実証実験を行いました。その中で研究論文作成までの長期的な計画を設定しリスクに備えた準備を行うスキルを身に着けました。また、課題にぶつかった際には仲間や先輩に上手くアドバイスを得ることの重要性を学びました。

- 学んだ内容
  - 情報工学（ネットワーク、データベース）
  - ソフトウェア設計と実装スキル
  - 機械学習モデル（決定木）の応用

#### [研究内容1] Home Energy Management System(HEMS)サービスのためのニューラルネットワークを用いた家庭電力データ特徴量抽出の研究

家庭におけるスマートメーターから得られる総電力データにおいて空調機やその他家電の電力データ特徴量をニューラルネットワークによって抽出することを試みる研究をしていました。
研究の中で既存の研究内容を読み解き理解する力、新規性を自ら論理的に構築する力、課題を自ら定めて解決方法を提案する力を養うことができました。

- 学んだ内容
  - システムデザイン工学
  - コンピュータサイエンス全般
  - 機械学習とその利用技術
  - スマートグリッド・スマートコミュニティ分野・技術