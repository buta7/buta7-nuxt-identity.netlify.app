# hige-nuxt-identity-netlify.app

* 動作確認済み(2020/09/11)
* 運用方法
    * RegistrationをInvite onlyにすることで保護できる(Sign Upリンクが消える)
    * https://app.netlify.com/sites/hige-nuxt-identity/identity から招待できる
        * Send reset password emailを送らないとパスワードが設定できない
            * これもよくわからないので結局最初はOpenにして作ってもらうのがよいか
    * ProviderにGoogleをセットするとこちらからも認証できる

## Build Setup

``` bash
# install dependencies
$ yarn install

# serve with hot reload at localhost:3000
$ yarn dev

# build for production and launch server
$ yarn build
$ yarn start

# generate static project
$ yarn generate
```

## Netlify

### Deploy settings

* Build command: npm run generate
* Publish directory: dist

### Identity

* 認証の有効化
    * Dashboard>Site Settings>Identity>Eable
* 招待のみにする(事前にサインアップしてユーザ作っておくこと)
    * Dashboard>Site Settings>Identity>Registragion
        * Registration preferences: Invite only
* ローカルデバッグ時の認証(screenshot/screenshot-local-login.png)
    * Development Settings
        * URL: https://hige-nuxt-identity.netlify.app/ > Set site's URL
* note
    * ひげ/おなか痛い

## Link

* [Using Netlify Identity in a Vue SPA without localStorage \- DEV](https://dev.to/jeremywynn/using-netlify-identity-in-a-vue-spa-without-localstorage-23ob)
* [jeremywynn/nuxt\-netlify\-identity: Nuxt with Netlify Identity and better state hydration](https://github.com/jeremywynn/nuxt-netlify-identity)
