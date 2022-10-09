---
title: "LIFF の解説"
---

## React について

## LIFF API について
開発上の注意点は [LIFFアプリ開発ガイドライン](https://developers.line.biz/ja/docs/liff/development-guidelines/) を確認してください
APIの詳細は [LIFF v2 APIリファレンス](https://developers.line.biz/ja/reference/liff/) を確認してください

### [liff.init()](https://developers.line.biz/ja/reference/liff/#initialize-liff-app) / [liff.isLoggedIn()](https://developers.line.biz/ja/reference/liff/#is-logged-in)

- liff.init()

> LIFFアプリを初期化します。このメソッドを実行すると、LIFF SDKの他のメソッドを実行できるようになります。このとき、LIFF SDKは、現在のユーザーのアクセストークンやIDトークンをLINEプラットフォームから取得します。

- liff.isLoggedIn()

> ユーザーがログインしているかどうかを取得します。

```js:App.js
liff
  .init({ liffId: process.env.REACT_APP_LIFF_ID })
  .then(() => {
    const isLogin = liff.isLoggedIn()
    // ...
    setLiffState([liff, isLogin])
  })
  .catch((err) => {
    console.error({ err })
  })
```

### [liff.login()](https://developers.line.biz/ja/reference/liff/#login) / [liff.logout()](https://developers.line.biz/ja/reference/liff/#logout)

- liff.login()

> 外部ブラウザおよびLINE内ブラウザ上で、ログイン処理を行います。

- liff.logout()

> ログアウトします。


```js:App.js
<LogoutButton
  liffObject={liffObject}
  logout={(() => {
    liffObject.logout()
    setLiffState([liff, false]);
  })}/>
<LoginButton
  liffObject={liffObject}
  login={(() => {
    liffObject.login().then(() => {
      setLiffState([liff, true]);
    })
  })}/>
```

### [liff.getProfile()](https://developers.line.biz/ja/reference/liff/#get-profile)

- liff.getProfile()

> 現在のユーザーのプロフィール情報を取得します。

```js:App.js
liff.getProfile().then((profile) => {
  // ...
  microCmsClient.create({
    // ...
    content: {
      userId: profile.userId
    }
  }).then((res) => console.log(res.id) )
})
```
