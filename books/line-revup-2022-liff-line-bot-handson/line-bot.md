---
title: "GAS の設定"
---

## SpreadSheet の作成

テンプレートの [spread sheet](https://docs.google.com/spreadsheets/d/1Y2OgfsZXwdNBha5sxr6oFRYOTuSmPJquHy9DZFQyzg8/copy) からスプレッドシートをコピーしてきます。

![](/images/books/line-revup-2022-liff-line-bot-handson/gas-copy-sheet-edit.png =400x)

今回は Google App Scripts を利用するので、開発用のエディタを開きます。
`拡張機能` > `App Script` から起動できます。

![](/images/books/line-revup-2022-liff-line-bot-handson/gas-open-app-script-edit.png)

## 環境変数の設定

`const.gs` の中にある `CHANNEL_ACCESS_TOKEN` / `LINE_USER_ID` / `SHEET_URL` の設定をします。
LINE Bot の設定画面から変更を行います。

| 定数 | 値 |
| :--- | :--- |
| `CHANNEL_ACCESS_TOKEN` | `Messaging API設定` > `チャネルアクセストークン` から `発行` をクリック<br />発行したトークンを貼り付けます。 |
| `LINE_USER_ID` | `チャネル基本設定` > `あなたのユーザーID` を貼り付けます。 |
| `SHEET_URL` | 先ほどコピーしたスプレッドシートの URL です。 |

![](/images/books/line-revup-2022-liff-line-bot-handson/gas-const-gs-edit.png)


## GAS の デプロイ

`デプロイ` > `新しいデプロイ` > `デプロイ` をクリックしてください。
※ アクセスできるユーザーを `全員` にしてください

`Advanced` > `Go to 無題のプロジェクト (unsafe)` > `Allow` をクリックします

| `Advanced` をクリック | `Allow` にて承認 |
| :---: | :---: |
| ![](/images/books/line-revup-2022-liff-line-bot-handson/gas-verified-app-edit.png =450x) | ![](/images/books/line-revup-2022-liff-line-bot-handson/gas-access-gas-edit.png =450x)

デプロイが完了すると、デプロイID と デプロイURL が表示されます。URL を利用するので、`ウェブアプリ` > `URL` をコピーします。

:::message alert
デプロイURL を LINE Bot と microCMS に登録していきます。
:::


### 2回目以降のデプロイ

`デプロイ` > `デプロイを管理` > `デプロイ` をクリックしてください。

![](/images/books/line-revup-2022-liff-line-bot-handson/gas-redeploy-top-edit.png =200x)

ペンのアイコンをクリックし、 `最新バージョン` へ編集を行います。

![](/images/books/line-revup-2022-liff-line-bot-handson/gas-redeploy-edit-edit.png)

## LINE Bot の設定

> > LINE Bot の設定

LIE Bot の設定画面から Wehbook の設定を行います。

`Webhook設定` > `Webhook URL` に `デプロイURL` を貼り付け `更新` をします。
保存が成功すると `Webhookの利用` のチェックボックスが出るので、有効にします。

![](/images/books/line-revup-2022-liff-line-bot-handson/line-bot-webhook-setting-edit.png)

`Messaging API設定` > `応答メッセージ` > `編集` から LINE Official Account Manager から応答設定を行います。
`詳細設定` > `応答メッセージ` を オフ / `詳細設定` > `Webhook` を オン にします。

![](/images/books/line-revup-2022-liff-line-bot-handson/gas-manager-line-biz-edit.png)

### LINE Bot の動作確認

> > LINE Bot の設定

`Messaging API設定` の QR または ID から、 Bot を追加します。
Bot にメッセージを送るとそのままのメッセージが返答されます。

## MicroCMS の webhook の登録

`API設定` > `Webhook` > `追加` から Webhook の設定をします。

1. `カスタム通知` をクリックします。
2. `Webhookの識別名を設定してください。(任意)` を `spread sheet` にします
3. `任意のURLに対してAPIやコンテンツの更新をPOSTリクエストで通知します。詳しくはドキュメントをご確認ください。` に `デプロイURL` を貼り付けます。
    - LINE Bot の webhook にコピーしたものです
4. `通知タイミングの設定` の下記の項目のみチェックを有効にします。
  `コンテンツ編集画面による操作` / `APIによる操作`

![](/images/books/line-revup-2022-liff-line-bot-handson/gas-micro-cms-webhook-edit.png)

### 動作確認
管理画面から microCMS の値を変更すると、Spreadsheet にログが保存され、 LINE Bot にメッセージが届きます。
