---
title: "LINE Developers の設定"
---

:::message alert
TODO: LIFF / LINE Bot の画面を混乱しないように修正する
:::

## LINE Bot / LIFF の開発準備

LINE Bot / LIFF の開発を行う上で、 LINE Developers のログインが必要になります。
また、初回ログインの場合は、開発アカウントの作成が必要になります。

- [LINE Developersコンソールにログインする](https://developers.line.biz/ja/docs/line-developers-console/login-account/#log-in-to-line-developers-console)
- [開発者アカウントを作成する（初回ログイン時のみ）](https://developers.line.biz/ja/docs/line-developers-console/login-account/#register-as-developer)

## LINE Bot の設定
LINE Bot は 「Messaging API」から設定を行います。

以下の値を設定し、「LINE公式アカウント利用規約」と「LINE公式アカウントAPI利用規約」に同意をし、登録します。
※ チャンネル名に、 LINE が含まれるメッセージは設定できません。

| ラベル | 値 |
| :--- | :--- |
| 会社・事業者の所在国・地域 | 日本 |
| チャネル名 | Rev UP 2022 |
| チャネル説明 | Rev UP 2022 アプリです |
| 大業種 | 個人 |
| 小業種 | 個人(その他) |

## LIFF の設定

LIFF は 「LINEログイン」 から設定を行います。
以下の値を設定し、「LINE開発者契約」に同意をし、登録します。
※ チャンネル名に、 LINE が含まれるメッセージは設定できません。

| ラベル | 値 |
| :--- | :--- |
| 会社・事業者の所在国・地域 | 日本 |
| チャネル名 | Rev UP 2022 Login |
| チャネル説明 | Rev UP 2022 Login アプリです |
| アプリタイプ | ウェブアプリ |

チャネル基本設定 > リンクされたボット > `Rev UP 2022` を指定することで、 LIFF 利用時に自動で LINE Bot を追加することができます。
