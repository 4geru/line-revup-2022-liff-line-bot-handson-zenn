---
title: "Github pages の設定"
---

## Github pages を公開する
### Github pages とは

> Hosted directly from your GitHub repository. Just edit, push, and your changes are live.
> GitHub リポジトリから直接ホストされます。 編集してプッシュするだけで、変更が反映されます。

[GitHub Pages | Websites for you and your projects, hosted directly from your GitHub repository. Just edit, push, and your changes are live.](https://pages.github.com/)

## project を fork する

[4geru/line-revup-2022-liff-line-bot-handson](https://github.com/4geru/line-revup-2022-liff-line-bot-handson) に移動し、リポジトリを fork します。

![](/images/books/line-revup-2022-liff-line-bot-handson/liff-fork-github-edit.png)

![](/images/books/line-revup-2022-liff-line-bot-handson/liff-confirm-github-edit.png)

### LIFF の登録

公開したページを LIFF のリダイレクト先に設定します。

LIFF アプリからの作成は、LIFF タブから `追加` ボタンを押します

![](/images/books/line-revup-2022-liff-line-bot-handson/line-liff-create-edit.png)

| ラベル | 値 |
| :--- | :--- |
| LIFFアプリ名 | Rev UP 2022 LIFF
| サイズ | Tall
| エンドポイントURL | github pages のリンク
| Scope | ✅ profile
| ボットリンク機能 | On (Aggressive)

### 公開の仕方
先ほど fork したリポジトリのページに遷移し、 clone します。
clone するリポジトリの情報は、github の fork からコピーします。

![](/images/books/line-revup-2022-liff-line-bot-handson/liff-github-clone-edit.png)

お使いのターミナルから、git clone コマンドを利用し、ローカルで必要なものをセットアップします。

```sh
git clone https://github.com/USER_NAME/line-revup-2022-liff-line-bot-handson.git
cd line-revup-2022-liff-line-bot-handson
```

## 環境変数の設定

.env.sample を元に .env を作成し、必要な情報を記入します。

```sh
cp .env.sample .env
```

| 環境変数名 | 値 |
| :--- | :--- |
| REACT_APP_LIFF_ID | `LIFF の設定ページ` > `LIFF` > `LIFF ID` をコピーします |
| REACT_APP_MICRO_CMS_SERVICE_DOMAIN | 作成した microCMS のサービスの URL の一部 <br /> `https://xxxxxxxxxx.microcms.io/apis/liff` |
| REACT_APP_MICRO_CMS_API_KEY | microCMS の API キーを設定します。 API キーは下記の動画の場所にあります。 |

![](/images/books/line-revup-2022-liff-line-bot-handson/liff-micro-cms-show-api-key-edit.png)

## デプロイ

必要なパッケージをインストールし、github に deploy を行います。

```sh
npm install
npm run deploy
```

`Visit site` をクリックすると、deploy を行ったページを確認できます

![](/images/books/line-revup-2022-liff-line-bot-handson/liff-github-check-deployed-unlogin-page.png)

## 動作確認

LIFF の登録が完了すると LIFF URL が発行されます。
LIFF は PC のブラウザからログイン可能ですが、LINEのアプリブラウザからログインすると、一部分のみ表示されることがわかります。

| PC | LINE アプリ |
| :--- | :--- |
| ![](/images/books/line-revup-2022-liff-line-bot-handson/liff-github-check-deployed-pages.png =500x) | ![](/images/books/line-revup-2022-liff-line-bot-handson/liff-login-from-line-app-edit.jpeg =300x)
