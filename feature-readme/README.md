## Init

```
npm install
```
## Features

### 📝 Convert Markdown to PDF

[md-to-pdf](https://www.npmjs.com/package/md-to-pdf) PDF生成する。

```
npm run build:pdf
```

出力されるPDFは`pdf-configs/style.css`を編集することで任意のスタイルを設定可能。

### 💅 Lint text

[textlint](https://github.com/textlint/textlint) での自動校正が可能。

Lint検知

```
npm run lint
```

Lint修正

```
npm run fix-lint
```