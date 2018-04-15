# Google Cloud SQL for PostgreSQL

* PostgreSQL のバージョンは 9.6.6(2018-04-15 時点)

## クイックスタート

https://cloud.google.com/sql/docs/postgres/quickstart?hl=ja

* `gcloud sql connect <インスタンス名> --connect=postgres`
  * 手元の端末で実行するには psql コマンドがインストールされている必要がある

## IP アドレスを使用して PSQL クライアントを接続する

https://cloud.google.com/sql/docs/postgres/connect-admin-ip?hl=ja

うまくいかんかった

## Cloud SQL Proxy を使用して PSQL クライアントに接続する

https://cloud.google.com/sql/docs/postgres/connect-admin-proxy?hl=ja

うまくいかんかった。。

## 参考

* 外部アプリケーションのための接続オプション
  * https://cloud.google.com/sql/docs/postgres/external-connection-methods?hl=ja
* Cloud SQL Proxy について
  * https://cloud.google.com/sql/docs/postgres/sql-proxy?hl=ja
* Google Cloud Platform Auth ガイド
  * https://cloud.google.com/docs/authentication?hl=ja
* Google Cloud Platform Auth ガイド
  * https://cloud.google.com/docs/authentication/production
* Setting Up Authentication for Server to Server Production Applications
  * https://cloud.google.com/docs/authentication?hl=ja
  * デフォルト承認情報

### あとで調べる

* Whitelisting your IP for incoming connection for 5 minutes...|
  * これを短くする方法
    * たぶん最初から IP アドレス追加しておけばよさそう?
      * `承認` に IP アドレス追加しても変わらない。というか最初の接続時に Whitelisting として追加されている
