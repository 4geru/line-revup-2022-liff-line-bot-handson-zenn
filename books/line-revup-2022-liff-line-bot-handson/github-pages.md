---
title: "Github pages の設定"
---

## project を fork する

[4geru/line-revup-2022-liff-line-bot-handson](https://github.com/4geru/line-revup-2022-liff-line-bot-handson) に移動し、リポジトリを fork します。

![](/images/books/line-revup-2022-liff-line-bot-handson/liff-fork-github-edit.png)

![](/images/books/line-revup-2022-liff-line-bot-handson/liff-confirm-github-edit.png)

## 環境変数の設定

![](/images/books/line-revup-2022-liff-line-bot-handson/liff-github-new-environment-edit.png)

| 環境変数名 | 値 |
| :--- | :--- |
| MICRO_CMS_SERVICE_DOMAIN | 作成した microCMS のサービスの URL の一部 <br /> `https://xxxxxxxxxx.microcms.io/apis/liff` |
| MICRO_CMS_API_KEY | microCMS の API キーを設定します。 API キーは下記の動画の場所にあります。 |

![](/images/books/line-revup-2022-liff-line-bot-handson/liff-micro-cms-show-api-key-edit.png)

## Github pages を公開する
### Github pages とは

:::message alert
TODO: 説明を書く
:::

### 公開の仕方
先ほど fork したリポジトリのページに遷移し、 clone します。
clone するリポジトリの情報は、github の fork からコピーします。

![](/images/books/line-revup-2022-liff-line-bot-handson/liff-github-clone-edit.png)

お使いのターミナルから、git clone コマンドを利用し、ローカルで必要なものをセットアップします。

```sh
git clone https://github.com/USER_NAME/line-revup-2022-liff-line-bot-handson.git
```

必要なパッケージをインストールし、github に deploy を行います。

```sh
npm install
npm run deploy
```

リポジトリの Settings > Pages を開き branch を main から gh-pages に変更します。

![](/images/books/line-revup-2022-liff-line-bot-handson/liff-github-open-github-pages-edit.png)

`Visit site` をクリックすると、deploy を行ったページを確認できます

![](/images/books/line-revup-2022-liff-line-bot-handson/liff-github-check-deployed-unlogin-page.png)

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

## microCMS の動作確認

LIFF の登録が完了すると LIFF URL が発行されます。
LINE アプリから LIFF のページを開くとアプリの確認が可能です。

![](/images/books/line-revup-2022-liff-line-bot-handson/liff-github-check-deployed-pages.png)
