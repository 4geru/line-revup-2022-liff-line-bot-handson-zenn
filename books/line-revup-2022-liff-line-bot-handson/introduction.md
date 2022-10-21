---
title: "今回のハンズオンについて"
---

## 事前準備

- node.js インストールをおねがいします。
  - [Download | Node.js](https://nodejs.org/en/download/)

必要なアカウントは以下の 4 種類が必要になります。
- microCMS
  - [microCMS アカウント作成](https://app.microcms.io/signup)
  - [microCMS ログイン](https://app.microcms.io/signin)
- github
  - [github](https://github.com/)
- google
  - [Google account](https://www.google.com/account/about/)
- line developers の登録
  - [LINE Developersコンソールにログインする](https://developers.line.biz/ja/docs/line-developers-console/login-account/#log-in-to-line-developers-console)
  - [開発者アカウントを作成する（初回ログイン時のみ）](https://developers.line.biz/ja/docs/line-developers-console/login-account/#register-as-developer)

## ハンズオンの対象者
- LINE API の利用経験がない方
- LIFF / LINE Bot どちらかで開発をおこなったことがある方
- microCMS の利用経験がない方

## 概要
今回のハンズオンでは LIFF と LINE Bot について学びます。
LIFF は、 LINE Front-end Framework の略で、LINE の情報をフロントエンドで使うためのものです。
Messaging API(以下： LINE Bot) は、 LINE 公式アカウントを通じて サーバーと LINE アプリ をつなげます。ユーザーからメッセージを受け取ると https の path に対して、 webhook を送信できます。

ブラウザ or LINE内ブラウザ からReact(LIFF) で変更した情報を microCMS に保存します。
保存した時の webhook アクションから LINE Bot を通じユーザーに通知を伝えます。

LIFF / LINE Bot の説明を深くしたいため、React / GAS(Google App Script) を非常にシンプルな作りにしています。React / GAS の依存をなくすため、データの保存先に microCMS にデータを保存します。

![](/images/books/line-revup-2022-liff-line-bot-handson/introduction-goal-image.jpeg)

LIFF は React の他にも Vue.js / Nuxt / Next など、他のフロントエンドのライブラリでも利用可能です。LINE Bot は GAS の他にも、さまざまな言語のwebサーバーのフレームワークで実装可能です。

React の tutorial([Quick Start](https://beta.reactjs.org/learn))を拡張したシンプルなアプリを作成します。
今回のハンズオンは終了後に是非お得意のフレームワークで置き換えてみてください。

## 画面
今回は、React の tutorial 機能を拡張したシンプルなアプリを作成します。
tutorial ページ [Quick Start](https://beta.reactjs.org/learn)

### ブラウザ画面
LINE ログインすると、LINEの表示名とアイコンが表示されます。

| PC | LINE内ブラウザ |
| :---: | :---: |
| ![](/images/books/line-revup-2022-liff-line-bot-handson/liff-github-check-deployed-pages.png =500x) | ![](/images/books/line-revup-2022-liff-line-bot-handson/liff-login-from-line-app-edit.jpeg =300x)

### 通知画面
フォームを保存すると、 LINE に通知が届きます。

![](/images/books/line-revup-2022-liff-line-bot-handson/line-bot-notice-view.jpeg =300x)

## 利用技術
- React
- GAS(Google App Script)
