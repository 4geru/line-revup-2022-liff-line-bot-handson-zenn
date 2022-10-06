---
title: "micro CMS の設定"
---

## コンテンツファイルのダウンロード

[gist](https://gist.github.com/4geru/938f6f8d5a9c994ed7e2c19830546e41) からフォーマットファイルをダウンロードします。
「Download ZIP」からダウンロードし、zip を解凍します。

![](/images/books/line-revup-2022-liff-line-bot-handson/micro-cms-gist.png)

## アカウントの作成

- [microCMS アカウント作成](https://app.microcms.io/signup)
- [microCMS ログイン](https://app.microcms.io/signin)

## サービスの作成

[サービスを作成](https://app.microcms.io/create-service) からサービスの作成を行います

![](/images/books/line-revup-2022-liff-line-bot-handson/micro-cms-create-service.png)

## コンテンツの作成

左側のコンテンツ（API）タブをクリックし、microCMSに保存するデータの形式を登録していきます。

`APIを作成` > `自分で決める` を選択します。

![](/images/books/line-revup-2022-liff-line-bot-handson/micro-cms-create-api.png)

1. APIキー「liff」 / エンドポイント「liff」 → 「次へ」
2. APIの型を選択 「リスト形式」 → 「次へ」
3. 「ファイルインポートする場合は `こちら` から。」のこちらからをクリックし、追加します。 → 「作成」
  先ほど解凍した zip ファイルのディレクトリから、 `microCmsSetting.json` を指定し登録します。

![](/images/books/line-revup-2022-liff-line-bot-handson/micro-cms-setup-api.png)

ダウンロードが完了すると以下のような状態になります。
作成ボタンをクリックし、コンテンツの作成を完了させます。

![](/images/books/line-revup-2022-liff-line-bot-handson/micro-cms-check-api.png)
