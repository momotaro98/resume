## Status

[![textlint](https://img.shields.io/github/workflow/status/momotaro98/resume/lint%20text?label=textlint&logo=github)](https://github.com/momotaro98/resume/actions?query=workflow%3A%22lint+text%22)
[![build pdf](https://img.shields.io/github/workflow/status/momotaro98/resume/build%20pdf?label=build%20pdf&logo=github&color=blue)](https://github.com/momotaro98/resume/actions?query=workflow%3A%22build+pdf%22)


## Setting up

```
npm install
```
## Features

### 📝 Convert Markdown to PDF

[md-to-pdf](https://www.npmjs.com/package/md-to-pdf) にてPDF生成をする。

```
npm run build:pdf
```

出力されるPDFは`pdf-configs/style.css`を編集することで任意のスタイルを設定可能。

### 💅 Lint text

[textlint](https://github.com/textlint/textlint) にて文章の自動校正をする。

Lint検知

```
npm run lint
```

Lint修正

```
npm run fix-lint
```

### 🛠 Create release

`v**` tagをつけてpushするとGitHub Actionsでビルドが走り、PDFの生成、Releaseの作成、AssetsへPDFの登録が実行される。

```
$ git commit -m "update job"
$ git tag v1.0.0
$ git push origin --tags
```

### 📆 Remind update

GitHub Actionsのschedule triggerで定期的に職務経歴書の内容更新を促すissueが自動生成される。

Issue発行の頻度変更、Job停止は[.github/workflows/create-issue.yml](../.github/workflows/create-issue.yml)で編集できる。

Issue内容は[.github/ISSUE_TEMPLATE.md](../.github/ISSUE_TEMPLATE.md)で編集できる。