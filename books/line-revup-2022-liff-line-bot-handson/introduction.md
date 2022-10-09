---
title: "今回のハンズオンについて"
---

## ハンズオンの対象者
- LINE API の利用経験がない方
- LIFF / LINE Bot どちらかで開発をおこなったことがある方
- microCMS の利用経験がない方

## 概要について

シンプルな React(LIFF) / LINE Bot を使った技術のハンズオンをします。
LIFF / LINE Bot が独立しているので、別の React を Next や GAS を Lambda などに置き換えることが簡単にできます。

![](/images/books/line-revup-2022-liff-line-bot-handson/introduction-goal-image.jpeg)

## ハンズオンで作るもの

React の tutorial 機能を拡張したシンプルなアプリを作成します。
tutorial ページ [Quick Start](https://beta.reactjs.org/learn)

React(LIFF) で変更した情報を microCMS に保存します。
保存した時の webhook アクションから LINE Bot を通じユーザーに通知を伝えます。

## 事前準備
:::message alert
TODO: アカウントの登録方法を書く
TODO: 事前にユーザーにお伝えする手段を考える
:::

必要なアカウントは以下の 3 種類が必要になります。
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
- React
- Google App Script

:::message alert
全体的にパッと見て
- TODO: github pages にサンプルの URL あった方がいいかな
- DONE: 最初に用語集みたいなのを作った方がいいかな
  - A. 最後に書き込む
- DONE: コピーする箇所が多いので、どこの情報をコピーしたのかわかりやすくしたい
  - A. コピーする値に名前をつけていく
- DONE: 手を動かすだけなので、課題を設定したい
  - A. microCMS に count を置いて、カウントアップ / ダウンとかできるようにする
  - A. LINE Bot のメッセージをアレンジできるようにする
- DONE: microCMS の post の設定
- TODO: package.json の homepage のリンク
:::