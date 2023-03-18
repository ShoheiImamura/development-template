# プロダクト名

プロダクトの概要を簡単に説明します。

## ディレクトリ構造

下記は、本プロダクトのディレクトリ構造です。

```shell
.
├ infra/ # dockerfile など
├ mkdocs/ # ドキュメント
├ src/ # 開発用 Laravel
├ template/ # デザイン確認用 nuxt , vue
├ Makefile
├ docker-compose.yaml
└ README.md
```

## ローカル環境で動かす方法

 make up コマンドで全てのアプリケーションが起動します。
```shell
$ make up
```

コンテナ内へログインする場合は、下記コマンドを入力します。
```shell
$ docker-compose exec app bash
```

#### APP

- `APP_URL`: プロダクトのURL。デフォルトは http://localhost です。

#### DB

- `DB_CONNECTION`: Laravel が使用するデータベースの種類。デフォルトは mysql です。
- `DB_HOST`: 接続先のホスト名またはIPアドレス。デフォルトは db です。
- `DB_PORT`: データベースのポート番号。デフォルトは 3306 です。
- `DB_DATABASE`: データベース名。デフォルトは laravel です。
- `DB_USERNAME`: データベースに接続する際のユーザー名。デフォルトは phper です。
- `DB_PASSWORD`: データベースに接続する際のパスワード。デフォルトは secret です。

#### MAILHOG

- `MAILHOG_PUBLISHED_PORT`: MailHogの公開用ポート番号。デフォルトは 8025 です。

#### WEB

- `WEB_PUBLISHED_PORT`: Webサーバーの公開用ポート番号。デフォルトは 80 です。

### 開発環境

本プロダクトは、Laravel と Nuxt.js を組み合わせたWebアプリケーションです。Laravelのバックエンドと、Nuxt.jsのフロントエンドが含まれます。また、MkDocsでのドキュメント管理を行っています。

| サービス | version |
| :------- | :------ |
| Nginx    | 1.18    |
| PHP      | 8.1     |
| Laravel  | 10.x    |
| MySQL    | 8.0     |
| Nuxt.js  | 3.x     |
| MkDocs   | 1.4     |
