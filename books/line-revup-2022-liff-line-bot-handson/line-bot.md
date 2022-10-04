---
title: "GAS の設定"
---

## SpreadSheet をコピーしてくる

[spread sheet](https://docs.google.com/spreadsheets/d/1Y2OgfsZXwdNBha5sxr6oFRYOTuSmPJquHy9DZFQyzg8/copy) からスプレッドシートをコピーしてきます。

![](/images/books/line-revup-2022-liff-line-bot-handson/gas-copy-sheet-edit.png)

`拡張機能` > `App Script` を起動します

![](/images/books/line-revup-2022-liff-line-bot-handson/gas-open-app-script-edit.png)

## 環境変数の設定

`const.gs` の中にある [1] `CHANNEL_ACCESS_TOKEN` / [2] `LINE_USER_ID` の設定をします。
LINE Bot の設定画面から変更を行います。

| 定数 | 値 |
| :--- | :--- |
| [1] `CHANNEL_ACCESS_TOKEN` | `Messaging API設定` > `チャネルアクセストークン` から `発行` をクリック<br />発行したトークンを貼り付けます。
| [2] `LINE_USER_ID` | `チャネル基本設定` > `あなたのユーザーID` を貼り付けます。

![](/images/books/line-revup-2022-liff-line-bot-handson/gas-const-gs-edit.png)


## GAS の デプロイ

`デプロイ` > `新しいデプロイ` > `デプロイ` をクリックしてください。
※ アクセスできるユーザーを `全員` にしてください

`Advanced` > `Go to 無題のプロジェクト (unsafe)` > `Allow` をクリックします

| `Advanced` をクリック | `Allow` にて承認 |
| :---: | :---: |
| ![](/images/books/line-revup-2022-liff-line-bot-handson/gas-verified-app-edit.png =450x) | ![](/images/books/line-revup-2022-liff-line-bot-handson/gas-access-gas-edit.png =450x)

`ウェブアプリ` > `URL` をコピーします

## LINE Bot の設定

LINE Bot の設定
`Messaging API設定` > `応答メッセージ` > `編集` から LINE Official Account Manager から応答設定を行います。
`詳細設定` > `応答メッセージ` を オフ / `詳細設定` > `Webhook` を オン にします。

![](/images/books/line-revup-2022-liff-line-bot-handson/gas-manager-line-biz-edit.png)

### LINE Bot の動作確認

## MicroCMS の webhook の登録

`API設定` > `Webhook` > `追加` から Webhook の設定をします。

[1] `Webhookの識別名を設定してください。(任意)` を `spread sheet` にします
[2] `任意のURLに対してAPIやコンテンツの更新をPOSTリクエストで通知します。詳しくはドキュメントをご確認ください。` に `GAS のコピー` を貼り付けます。
[3] `通知タイミングの設定` の下記の項目のチェックを外します。
  - `レビューによる公開`
  - `予約設定による操作`
  - `コンテンツの並び替え`
  - `コンテンツIDの変更`
  - `公開日時の変更`

![](/images/books/line-revup-2022-liff-line-bot-handson/gas-micro-cms-webhook-edit.png)

### MicroCMS の動作確認
