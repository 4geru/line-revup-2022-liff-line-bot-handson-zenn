---
title: "LINE Bot の解説"
---

## microCMS からのリクエスト

[コンテンツのWebhookを設定](https://document.microcms.io/manual/webhook-setting)

## LINE Bot からのリクエスト
LINE Bot では、ユーザーから LINE Bot にきたメッセージを返す replyMessage と LINE Bot からメッセージを送信する pushMessage が存在します。

### replyMessage

[応答メッセージを送る](https://developers.line.biz/ja/reference/messaging-api/#send-reply-message)

App Script > replyMessage に書かれています。

:::details replyMessage
```js
const replyMessage = (replyToken, messages) => {
  UrlFetchApp.fetch('https://api.line.me/v2/bot/message/reply', { // = LINE Messaging APIの利用に必要な固定URL
     'headers': {
       'Content-Type': 'application/json; charset=UTF-8',
       'Authorization': 'Bearer ' + CHANNEL_ACCESS_TOKEN, // = LINE返信メッセージに必要な固定URL
     },
     'method': 'post',
     'payload': JSON.stringify({
       'replyToken': replyToken, // = リプライトークン
       'messages': messages,
     }),
   });
}
```
:::

### pushMessage

[プッシュメッセージを送る](https://developers.line.biz/ja/reference/messaging-api/#send-push-message)

pushMessage は、月 1000 件を超えると有料になるので注意して利用してください。[料金プラン](https://www.linebiz.com/jp/service/line-official-account/plan/)

App Script > requestFromLineAPI に書かれています。
LINE の webhook の設定がされている時のみ利用可能です。

:::details requestFromLineAPI
```js
const pushMessage = (userId, messages) => {
  UrlFetchApp.fetch('https://api.line.me/v2/bot/message/push', { // = LINE Messaging APIの利用に必要な固定URL
     'headers': {
       'Content-Type': 'application/json; charset=UTF-8',
       'Authorization': 'Bearer ' + CHANNEL_ACCESS_TOKEN, // = LINE返信メッセージに必要な固定URL
     },
     'method': 'post',
     'payload': JSON.stringify({
        to: userId,　//ユーザーID
        messages: messages
     }),
   });
}
```
:::
