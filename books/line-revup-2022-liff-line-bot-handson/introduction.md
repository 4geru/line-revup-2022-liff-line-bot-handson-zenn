---
title: "今回のハンズオンについて"
---

## はじめに

事前準備

## ハンズオンの対象者
- LINE API の利用経験がない方
- LIFF / LINE Bot どちらかで開発をおこなったことがある方
- microCMS の利用経験がない方

## 概要について

:::message alert
- TODO: 概要についての日本語が少しおかしい気が。LINE BotがBackendで、LIFFがFrontendで、それぞれ簡単に代替できるということがあまり伝わらない気がしました。
- TODO: 唐突な Next / Lambda などのワードがあるので飛躍しすぎている
:::

React の tutorial 機能を拡張したシンプルなアプリを作成します。
tutorial ページ [Quick Start](https://beta.reactjs.org/learn)

React(LIFF) で変更した情報を microCMS に保存します。
保存した時の webhook アクションから LINE Bot を通じユーザーに通知を伝えます。

---

シンプルな React(LIFF) / LINE Bot を使った技術のハンズオンをします。
LIFF / LINE Bot が独立しているので、別の React を Next や GAS を Lambda などに置き換えることが簡単にできます。

![](/images/books/line-revup-2022-liff-line-bot-handson/introduction-goal-image.jpeg)

## 完成イメージ

ブラウザ or LINE内ブラウザ からアクセスしフォームを保存すると LINE Bot にメッセージが届くようにします。

### ブラウザ画面
LINE ログインすると、LINEの表示名とアイコンが表示されます。

| PC | LINE内ブラウザ |
| :---: | :---: |
| ![](/images/books/line-revup-2022-liff-line-bot-handson/liff-github-check-deployed-pages.png =500x) | ![](/images/books/line-revup-2022-liff-line-bot-handson/liff-login-from-line-app-edit.jpeg =300x)

### 通知画面
フォームを保存すると、 LINE に通知が届きます。

![](/images/books/line-revup-2022-liff-line-bot-handson/line-bot-notice-view.jpeg =300x)

## 事前準備

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


## 利用技術
:::message alert
- TODO: node / npm の環境構築までしてね
:::

- React
- Google App Script
