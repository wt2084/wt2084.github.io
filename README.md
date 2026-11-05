# wt2084.github.io

AI・プロダクト・技術についてのメモと資料の公開サイト。
`https://wt2084.github.io/`

## 置き場所

```
.
├── index.html                    トップ（一覧）
├── ogp.png                       トップのカード画像
├── assets/site.css               共通の見た目
├── ai/
│   ├── index.html                カテゴリの一覧
│   └── code-review-2026-10/      1つの資料ごとにフォルダを切る
│       ├── index.html
│       ├── deck.pdf
│       ├── ogp.png
│       └── *.png
└── demos/                        動くもの（ビルド成果物だけ。いまは空）
```

## 足し方

1. カテゴリの下に `yyyy-mm-dd-topic`（または `topic-yyyy-mm`）でフォルダを作る
2. その中に `index.html`・PDF・画像・`ogp.png`（1200×630）を置く
3. `index.html`（トップ）とカテゴリの `index.html` の一覧に1件足す
4. commit して push（GitHub Pages が1分ほどで反映する）

新しいカテゴリを増やすときは、フォルダと `index.html` を作り、トップの「カテゴリ」に足す。

## 決めごと

- **PDFはブラウザのビューアで開く**（Content-Type は自動で `application/pdf`）。埋め込みは `<iframe src="deck.pdf#view=FitH">`
- **OGPは絶対URL**で書く。`https://wt2084.github.io/...`。1200×630 の PNG を用意する
- **コードのソースはこのリポジトリに置かない。** 1プロジェクト＝1リポジトリにして、動くもの（ビルド成果物）だけ `demos/` に置く
- **公開されるリポジトリ**なので、社内の資料・個人情報・未公開の情報は入れない

## ローカルで見る

```sh
python3 -m http.server 8000
# http://localhost:8000/
```

`/assets/...` や `/ai/...` の絶対パスで書いているので、ファイルを直接開かずサーバー経由で見る。
