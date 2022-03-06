# 職務経歴書

## 基本情報

|key|value|
|---|-----|
|名前| 穴澤 伸太郎 (旧姓 池田) |
|生年| 1991年 |
|居住地| 東京都杉並区 |
|最終学歴| 慶應義塾大学大学院 理工学部 情報工学科 |

## 各種アカウント

|key|value|
|---|-----|
|GitHub|[momotaro98](https://github.com/momotaro98)|
|Qiita|[momotaro98](https://qiita.com/momotaro98)|
|Twitter|[@momotaro98_](https://twitter.com/momotaro98_)|
|Speaker Deck|[momotaro98](https://speakerdeck.com/momotaro98)|

## 自己PR

- プロダクトにおける要件定義・設計・開発・構築・運用のすべてを過去2つの職歴とも経験している。
- 英語を使った業務経験を過去2つの職歴とも経験している。
- 組織設計・リーンアジャイル手法といったエンジニアリングマネジメントへの関心が高い。
- Qiita,技術ブロクに継続的に投稿している。
- OSSへのコントリビュートを継続的に行っている。

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

### ツール、その他**
  - CI/CD (TeamCity/Jenkins/CircleCI/GitLabCI/GitHub Actions)
  - Ticket management (JIRA/Trello/Backlog)
  - Document management (Confluence/GoogleDoc/Notion)

## 職務経歴詳細

### 株式会社レアジョブ（現職）: 2019/11 ~

#### 概要

社内でプラットフォームと呼ばれるビジネスサービス基盤を担当するチームにて、バックエンド兼DevOpsエンジニアとして開発・運用をしていました。

#### 役割と期間

#### 詳細

- 検索サービスリプレース開発・運用

既存で存在していたモノリシックシステムに対する「他機能に影響を与えていた検索による既存MySQL DBへの負荷を取り除く」,「変更・リリース容易性を得る」,「レッスン・講師検索機能における業務仕様を明確化する」という課題の解決のために、新規にマイクロサービスとして検索サービスAPIを切り出すことを、設計・実装・構築・運用、すべてに責任を持ち目的を達成することができました。
全社的な大きなリプレースプロジェクトであったため、設計からリリースまでに1年3ヶ月かけて実施しました。
レアジョブ英会話における検索サービスは、複雑な既存仕様を持つレッスンドメイン、講師ドメイン、生徒ドメイン、と3つのドメインが交わるサービスであり、様々な社内のチームと強調し仕様を整理しながら進めました。
検索サービスAPIのデータベースにはElasticsearchとRedisを採用、実装にはGo言語を採用しました。技術的な課題として、レッスン検索と講師検索というビジネス要件のためにElasticsearchでのデータスキーマをどのように持つか、どのように過去レッスンとして検索対象にならないようにするか、ElasticsearchのインデックスのMapping変更をどのように実現するか、などがありどれもひとつひとつ解決していきました。

- レッスン基盤サービス開発

レアジョブ社のサービスにて共通で存在するレッスン・カウンセリングの予約管理共通基盤サービスの開発・運用を担当していました。既存機能の要件定義とDBスキーマ変更、既存インフラからインフラコード(CloudFormation)を使ったインフラへの変更対応、負荷試験を新規に仕組み化し実施、CICDを既存の複雑な状態のものからAWS CodePipeline、CodeDeployを利用し改善するタスクを自ら提案し実施しました。

- レッスンデータの新規システムへのマイグレーション

既存で存在していたモノリシックシステムで (TODO つづき) 。

- 生徒・講師アカウントのマイグレーション

TODO

- 決済基盤サービス/決済系バックオフィスツール開発

TODO

-----

### 楽天グループ株式会社: 2017/04 ~ 2019/10

物流システム開発部署に所属
Order Management Systemと呼ばれる受注管理システムの開発・運用

ECサイト店舗向け受注管理システムの開発を担当。
受注業務のアプリケーションをメインにシステム設計&開発。C# .NETのプロダクトになります。
アジャイル開発の中ではスクラムマスタ兼務でプロジェクトに貢献。また、CI/CDの改善や運用システムをAzureを利用し開発することも担当。
運用面では受注業務だけでなく商品管理業務、在庫管理業務などの機能面も把握しカスタマー対応や障害対応を経験。

**より詳細な内容は以下のブログ記事を参照ください。**

https://ochataro.hateblo.jp/entry/2019/10/31/152634

-----

### 副業

- Mixlunch
  - Mixlunchは新卒楽天期の同期と起業を目標に作ったサービスです。ローンチまでは達成しましたが集客ができずビジネスモデルを再検討後マネタイズ設計が曖昧とわかりサービス継続を断念しました。
  - サービスLPページ https://www.mixlunch.com/
  - GitHub URL 
    - バックエンドAPI (Go): https://github.com/momotaro98/mixlunch-service-apis
    - BFF API (Node.js): https://github.com/momotaro98/mixlunch-bff-apis

-----

### 大学・大学院での研究 2014/04 ~ 2017/03
