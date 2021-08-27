
テンプレ init

```
$ npx @docusaurus/init@latest init [name] [template]
```

2021/08/27

[Docusaurusu themes](https://docusaurus.io/docs/api/themes) を読む限り

基本 template は classic を使ったほうが良さそう


```
$ npx @docusaurus/init@latest init hogehoge classic
```


```
$ tree -I "node_modules" hogehoge
hogehoge
├── README.md
├── babel.config.js
├── blog ## <= ブログ、不要なら削除
│   ├── 2019-05-28-first-blog-post.md
│   ├── 2019-05-29-long-blog-post.md
│   ├── 2021-08-01-mdx-blog-post.mdx
│   ├── 2021-08-26-welcome
│   │   ├── docusaurus-plushie-banner.jpeg
│   │   └── index.md
│   └── authors.yml
├── docs ## <= ドキュメント、sidebar.jsで、順番変更可能
│   ├── intro.md
│   ├── tutorial-basics
│   │   ├── _category_.json
│   │   ├── congratulations.md
│   │   ├── create-a-blog-post.md
│   │   ├── create-a-document.md
│   │   ├── create-a-page.md
│   │   ├── deploy-your-site.md
│   │   └── markdown-features.mdx
│   └── tutorial-extras
│       ├── _category_.json
│       ├── manage-docs-versions.md
│       └── translate-your-site.md
├── docusaurus.config.js ## <= サイトの設定を含む設定ファイル
├── package.json
├── sidebars.js ## <= サイドバーの順番指定用のjs
├── src ## <= ドキュメント以外のファイル。厳密にココに置く必要はないけど、ここにおいておくというルールがあると、指定しやすい
│   ├── components
│   │   ├── HomepageFeatures.js
│   │   └── HomepageFeatures.module.css
│   ├── css
│   │   └── custom.css
│   └── pages ## <= ウェブサイトのページになる
│       ├── index.js
│       ├── index.module.css
│       └── markdown-page.md
├── static ## 静的ディレクトリ。ここにあるコンテンツは、最終的なビルドディレクトリのrootにcopyされる
│   └── img
│       ├── docusaurus.png
│       ├── favicon.ico
│       ├── logo.svg
│       ├── tutorial
│       │   ├── docsVersionDropdown.png
│       │   └── localeDropdown.png
│       ├── undraw_docusaurus_mountain.svg
│       ├── undraw_docusaurus_react.svg
│       └── undraw_docusaurus_tree.svg
└── yarn.lock

12 directories, 37 files
```
