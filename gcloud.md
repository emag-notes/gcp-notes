# gcloud

## コンフィグ

### 設定されたプロジェクトの出力

``` bash
gcloud config list project --format "value(core.project)"
```

## サービス

### 利用可能サービス一覧

以下で調べてから:

``` bash
gcloud services list --available
```

### サービスの有効化

``` bash
gcloud services enable <サービス名>
```

例えば GKE の場合は以下

``` bash
gcloud services enable container.googleapis.com
```

### 参考

* https://cloud.google.com/service-management/list-services?hl=ja
* https://cloud.google.com/service-management/enable-disable?hl=ja

## 課金

### アカウント一覧

``` bash
gcloud beta billing accounts list
```

### アカウント ID にひもづいているプロジェクト

``` bash
gcloud beta billing projects list --billing-account <アカウント ID>
```

https://cloud.google.com/sdk/gcloud/reference/beta/billing/

### アカウント ID とプロジェクトのひもづけ

``` bash
gcloud beta billing projects link <プロジェクト ID> --billing-account <アカウント ID>
```
