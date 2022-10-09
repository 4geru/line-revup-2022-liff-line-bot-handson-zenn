---
title: "LINE Developers の設定"
---

## LINE Bot / LIFF の開発準備

LINE Bot / LIFF の開発を行う上で、 LINE Developers のログインが必要になります。
また、初回ログインの場合は、開発アカウントの作成が必要になります。

- [LINE Developersコンソールにログインする](https://developers.line.biz/ja/docs/line-developers-console/login-account/#log-in-to-line-developers-console)
- [開発者アカウントを作成する（初回ログイン時のみ）](https://developers.line.biz/ja/docs/line-developers-console/login-account/#register-as-developer)

:::message
* 英語表記になっている場合は、右下の Tab から言語の切り替えが可能です

![](/images/books/line-revup-2022-liff-line-bot-handson/line-language-setting.png =300x)
:::

## LINE Bot の設定
LINE Bot は、[LINE console](https://developers.line.biz/console/) から「Messaging API」から設定を行います。

以下の値を設定し、「LINE公式アカウント利用規約」と「LINE公式アカウントAPI利用規約」に同意をし、登録します。
※ チャンネル名に、 LINE が含まれるメッセージは設定できません。

| ラベル | 値 |
| :--- | :--- |
| 会社・事業者の所在国・地域 | 日本 |
| チャネル名 | Rev UP 2022 Bot |
| チャネル説明 | Rev UP 2022 Bot アプリです |
| 大業種 | 個人 |
| 小業種 | 個人(その他) |

## LIFF の設定

次に、LIFF の設定を行います。
[LINE console](https://developers.line.biz/console/) から「新規チャンネルの追加」をクリックし、 「LINEログイン」 を選択します。

![](/images/books/line-revup-2022-liff-line-bot-handson/line-create-new-account-edit.png)

以下の値を設定し、「LINE開発者契約」に同意をし、登録します。
※ チャンネル名に、 LINE が含まれるメッセージは設定できません。

| ラベル | 値 |
| :--- | :--- |
| 会社・事業者の所在国・地域 | 日本 |
| チャネル名 | Rev UP 2022 Login |
| チャネル説明 | Rev UP 2022 Login アプリです |
| アプリタイプ | ウェブアプリ |

チャネル基本設定 > リンクされたボット > `Rev UP 2022` を指定することで、 LIFF 利用時に自動で LINE Bot を追加することができます。

## LINE Bot と LIFF のアカウントの見分け方

LINE Bot のアカウント と LIFF のアカウントを見間違うことが多いので、注意してください。

### LINE Bot のアカウント
1. 名前が「Rev UP 2022 Bot」 になっている
2. Messaging API と記載がある

※ 今回のハンズオンでは「LINE Bot の設定ページ」と呼びます

![](/images/books/line-revup-2022-liff-line-bot-handson/line-bot-top-edit.png =300x)

### LIFF のアカウント
1. 名前が「Rev UP 2022 Login」 になっている
2. LINEログイン と記載がある

※ 今回のハンズオンでは「LIFF の設定ページ」と呼びます

![](/images/books/line-revup-2022-liff-line-bot-handson/line-login-top-edit.png =300x)
