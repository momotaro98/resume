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
|Speaker Deck|[momotaro98](https://speakerdeck.com/momotaro98)|

-----

## 自己PR

- プロダクト開発にて要件定義、設計、開発、構築、運用を通して担うことを過去2つの職歴とも経験している
- 業務でのチームメイトとの英会話コミュニケーションを過去2つの職歴とも経験している
- 技術記事の投稿や[ISUCON](https://isucon.net/)への参加を通して継続的な学習をしている
- OSSへのコントリビュートを継続的に行っている
- 組織文化、開発者体験、リーン、アジャイルといったエンジニアリングマネジメントへの関心が高い

-----

## スキル

### 技術スタック

|名前| 経験年数 |備考|
|---|-----|---|
|Go| 4年 | WebApp, CLI, Library |
|C#| 3年 | .NET Framework |
|JavaScript| 2年 | Node.js/jQuery |
|TypeScript| 1年 | AWS CDK |
|Python| 2年 | Flask |
|MySQL| 3年 | |
|SQLServer| 2年 | |
|Redis| 3年 | Cluster on AWS ElastiCache |
|Elasticsearch| 3年 | Cluster on AWS OpenSearch |
|AWS| 3年 | CloudWatch/SNS/IAM/CloudFormation/CodePipeline/Deploy/Build/Route53/S3/API Gateway/Lambda/ALB/ECS Fargate/Aurora DB/SQS/OpenSearch/DynamoDB/ElastiCache/Batch/Beanstalk/Kinesis |
|Azure| 1年 | Azure Functions/Table Strage/Queue Storage/Cosmos DB |
|Firebase| 1年 | Auth/Storage/Site |
|Terraform| 1年 | |
|Ansible| 1年 | |

### ツール、その他
  - CI/CD (TeamCity/Jenkins/CircleCI/GitLabCI/GitHub Actions)
  - Ticket management (JIRA/Trello/Backlog)
  - Document management (Confluence/GoogleDoc/Notion)

-----

## 今後担いたいロール / 伸ばしたいスキル

* SRE / DevOps エンジニア
  * ビジネス貢献に関わるシステム指標を改善する仕組みの提供
  * プロダクトの非機能品質（パフォーマンス、セキュリティ、可用性、等）の向上への貢献
* エンジニアリングマネージャー
  * 開発者体験の向上のためのプロセスや組織の設計
  * 優れたチームを築き上げるためのコーチング、採用

-----

## 職務経歴詳細

### 株式会社レアジョブ（現職）: 2019/11 ~

#### 概要

社内でプラットフォームと呼ばれるビジネスサービス基盤を担当するチームにて、バックエンド兼DevOpsエンジニアとして開発・運用を担当。 また、フィリピン子会社に所属するエンジニアチームとの英語でのコミュニケーションを必要とするロールを担っていた。

#### 詳細

**検索サービスリプレース開発・運用**

[業務課題]  
既存で存在していたモノリシックシステムの特に検索機能において以下の課題が存在していた。
* MySQL DBへの負荷が支配的になっていた
* 変更リリースが容易ではない
* 既存の業務仕様が不明確で仕様を決めることができない

[担当範囲]   
その解決のため、新規にマイクロサービスとして検索サービスAPIを切り出す意思決定を組織で行い、その設計、実装、構築、運用すべてに責任を持ち業務課題解決の目的を達成することに貢献した。  
[進め方]  
検索サービスはレッスンドメイン、講師ドメイン、生徒ドメイン、と複雑な3つのドメインが交わるサービスだった。様々な社内のチームと協調し明らかになった仕様を都度ドキュメント化しながら進めた。業務委託のメンバーに対して背景と仕様の説明をしながらペアプロで実装することによりタスクの効率化を図った。  
[採用技術]  
検索サービスAPIのデータベースには講師の自己紹介文などのテキストベースのデータも存在していたこと、多くの検索条件が要件であったこと、検索リクエストのスケール性を持たせるためにElasticsearchを採用した。生徒ドメインのデータを持たせるキャッシュとしてRedisを採用し、APIアプリケーションの実装にはノウハウやチーム内共通ライブラリを持つGo言語を利用した。  
[技術的課題]  
技術的な課題として以下などが存在しひとつひとつ解決した。
* レッスン検索、講師検索、ブックマーク講師検索という異なった仕様の検索画面それぞれへ対応させるためにElasticsearchとRedisでデータスキーマをどのように持つか
* 既存モノリスDBとデータを同期させながら各ドメインのデータをどのように新規検索サービスDBへ連携させるか
* 負荷軽減のため過去のレッスンを検索対象とさせないためにどのような設計とするか
* Elasticsearchのクラスター構成、シャード数はどう決定するか
* 既存で作成済みのElasticsearchのインデックスのMapping変更をどのように実現するか
* SQSのスタンダードキューからHigh Throughput FIFOキューへどのように移行するか

*利用した技術スタック*
- Go、SAM、Lambda、Redis(ElastiCache)、Elasticsearch(OpenSearch)、SQS、MySQL(RDS AuroraDB)
- API Gateway、AWS Beanstalk、VPC Endpoint、GitLab CI

**レッスン基盤サービスAPI開発**

サービスプロダクトにて共通で存在するレッスン・カウンセリングの予約管理共通基盤サービスの開発・運用を担当した。
以下のような技術課題に対して、改善案を提案し実施した。
* e2eテストが存在せず、リグレッションが発生していた課題に対するCI上でのe2eテストの実現
* データ不整合が発生する課題に対するDBスキーマ変更を伴う段階的な修正対応
* 既存の手動で構築されたインフラからインフラコード（CloudFormation）で構築する変更対応
* 既存の複雑な管理状態のCICDからAWS CodePipeline、CodeDeployを利用した管理が集約されたものへの変更対応
* 実施記録が曖昧になっていた負荷試験の実行方法とレポートフォーマットを仕組み化
* アプリケーションログ形式改善、各種メトリクスの可視化ダッシュボード作成、それらのアラート設定対応

*利用した技術スタック*
- Go、ECS(Fargate)、ALB、MySQL(RDS AuroraDB)、API Gateway、GitLab CI、CodePipeline、CodeDeploy、CloudFormation

**決済基盤サービス/決済系バックオフィスツール開発**

[業務課題]  
* 社内のどのプロダクトでも利用できる共通決済機能を持つAPIが存在せず将来的な機能重複の無駄が存在していた
* 既存システムの決済情報管理機能はユーザー作業時間が長くかかり、かつ修正を加えるのが難しい状態になっていた
* 既存システムは特定の決済代行サービスに依存していた

[担当範囲]   
共通決済基盤サービスの開発運用に携わった。返金対応などのユーザーの決済に関わるバックオフィス業務用ツールの新規開発に対応するための機能の拡張を担当。また、共通基盤サービスの認証認可システムにおいてバックオフィスツールを利用する社内ユーザーのみが利用できるように機能を設計、実装担当した。開発にあたり、決済代行サービスのシステム仕様を読み込むことで共通決済基盤サービスの問題点を把握し不具合修正も実施した。

[技術的課題]  
* 特定の決済代行サービスに依存しない形で決済データモデルをどのように抽象化設計するか
* 一般ユーザーと管理者ユーザーを区別するアクセス制御をどのように設計するか
* 月時支払実行の負荷をどのように軽減させる設計にするか

*利用した技術スタック*
- Go、ECS(Fargate)、ALB、MySQL(RDS AuroraDB)、API Gateway、GitLab CI、CodePipeline、CodeDeploy、CloudFormation

-----

### 楽天グループ株式会社: 2017/04 ~ 2019/10

物流システム開発部署に所属し、Order Management System(OMS)と呼ばれるECサイト店舗向けの受注管理システムの開発と運用を担当。

受注業務のアプリケーションをメインにシステム設計・開発を担っていた。

* アジャイル開発の中ではプロダクトオーナーとスクラムマスタを兼務しプロジェクトに貢献
* 既存の複雑なCI/CDの仕組みをシンプルで管理しやすいように改善
* 複雑なプロダクトに関わるすべての機能を把握し、カスタマー問い合わせ対応と障害対応を経験
* チームメイトと英会話によるコミュニケーションを継続
* 業務委託社員のタスク管理業務を経験

**より詳細な職務内容は以下のブログ記事に記載しております**

https://ochataro.hateblo.jp/entry/2019/10/31/152634

*利用した技術スタック*
- C#、JavaScript、.NET Framework、Windows Server、SQLServer、Azure Functions

-----

### 副業

- "Mixlunch"と名付けたランチメートのマッチングサービスの開発とローンチ
  - Mixlunchは新卒時の同期と起業を目標に作ったサービス。ローンチまでは達成したが集客ができずサービス継続を断念
  - 開発担当システムのGitHub URL 
    - バックエンドAPI (Go): https://github.com/momotaro98/mixlunch-service-apis
    - BFF API (Node.js): https://github.com/momotaro98/mixlunch-bff-apis
  - その他
    - ランチメイトのマッチングバッチはPythonで機械学習モデル利用を想定し実装。(ソースコードは非公開）

*利用した技術スタック*
- Go、JavaScript(Node.js)、Python、Vue.js、Firebase Auth、Storage、AWS RDS(MySQL)、ECS、ALB