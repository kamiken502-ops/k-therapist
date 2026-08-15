# anime.k-therapist.com Jekyll版

既存のHTML/CSSサイトの見た目を維持しながら、GitHub Pages標準のJekyllでブログを生成できる構成です。

## 記事の追加

`_posts` に `YYYY-MM-DD-slug.md` という名前でMarkdownファイルを追加します。

```yaml
---
title: "記事タイトル"
description: "検索結果やSNSカードに表示する要約"
date: 2026-08-15 09:00:00 +0900
last_modified_at: 2026-08-15 09:00:00 +0900
category: "睡眠"
image: "/images/blog/example.jpg" # 任意
image_alt: "画像の説明"            # imageを使う場合に推奨
author: "神谷 健太"
---
```

本文はFront Matterの下にMarkdownで記述します。ファイル名の `slug` が `/blog/slug/` のURLになります。

## 非公開の下書き

公開前の記事は `_drafts` に保存します。現在のサンプル記事も `_drafts/stress-reaction.md` に置き、`published: false` を指定しているため、通常のGitHub Pages公開では表示されません。

公開するときは、内容を確認したうえで `published: false` を削除し、ファイル名を `YYYY-MM-DD-slug.md` に変更して `_posts` へ移します。

## ローカル確認

```sh
bundle install
bundle exec jekyll serve
```

ブラウザで `http://127.0.0.1:4000/` を開きます。

## GitHub Pagesへの反映

このフォルダの内容を、現在GitHub Pagesで公開しているブランチのルートへ配置します。GitHubの Pages 設定が「Deploy from a branch」の場合、push後にJekyllが自動で生成されます。

Decap CMS用の `/admin/` はまだ追加していません。ブログ表示と記事構造が安定した後の第2段階で追加できます。
