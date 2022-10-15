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

[サービスを作成](https://app.microcms.io/create-service) からサービスの作成を行います。
サービスの作成が完了すると `サービスにアクセスする` ボタンを押します。

![](/images/books/line-revup-2022-liff-line-bot-handson/micro-cms-create-service.png)

サービス名とサービスIDについて、公式には下記のように記載されています。

> サービス名にはmicroCMSの導入を考えているプロダクト名や組織名を入力すると良いでしょう。
サービスIDは管理画面のURL、APIのエンドポイントのサブドメインに設定される値です。

参照；[サービスの作成](https://document.microcms.io/manual/create-service)

## コンテンツの作成

左側のコンテンツ（API）タブをクリックし、microCMSに保存するデータの形式を登録していきます。

`APIを作成` > `自分で決める` を選択します。

![](/images/books/line-revup-2022-liff-line-bot-handson/micro-cms-create-api.png)

1. APIキー「liff」 / エンドポイント「liff」 → 「次へ」
2. APIの型を選択 「リスト形式」 → 「次へ」
3. 「ファイルインポートする場合は `こちら` から。」のこちらからをクリックし、追加します。 → 「作成」
  先ほど解凍した zip ファイルのディレクトリから、 `microCmsSetting.json` を指定し登録します。

![](/images/books/line-revup-2022-liff-line-bot-handson/micro-cms-setup-api.png)

APIスキーマについては、 [APIスキーマ設定](https://document.microcms.io/manual/api-model-settings) にまとまっています。

| APIスキーマ | 表示名 |
| :--- | :--- |
| フィールドID | APIレスポンスのプロパティ名です。
| 表示名 | コンテンツを入力する際に表示されます。
| 種類 | コンテンツを入力する際の入力フォームを指定することができます。<br/>[フィールドの詳細設定項目](https://document.microcms.io/manual/api-model-settings#h1993cddc9a) の値が登録可能です。

ダウンロードが完了すると以下のような状態になります。
`作成ボタン` をクリックし、コンテンツの作成を完了させます。

![](/images/books/line-revup-2022-liff-line-bot-handson/micro-cms-check-api.png)

| フィールド名 | 表示名 | |
| :--- | :--- | :--- |
| userId | LINE ユーザーID | LINE の userId<br />フィールドの設定：<br />1. 必須事項<br/>2. 詳細編集 > 重複を許可しない（ユニーク）
| title | タイトル | LIFF フォームから入力する値
| content | 本文 | LIFF フォームから入力する値

## API の設定

`1個の APIキー` > `default` をクリックし、下記のページに遷移します。
`デフォルト権限` を `POST` / `PATCH` を有効にします。

![](/images/books/line-revup-2022-liff-line-bot-handson/micro-cms-change-get-post-patch-edit.png)

:::message
- `変更` をすることを忘れないでください。
:::
