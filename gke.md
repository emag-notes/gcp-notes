# GKE

## kubectl のインストール

``` bash
gcloud components install kubectl
```

## クラスタの作成

``` bash
gcloud container clusters create [CLUSTER_NAME]
```

## クラスタ利用の認証情報の取得

> どっちをやればいいんだろう?

* gcloud container clusters get-credentials [CLUSTER_NAME]
  * `~/.kube/config` が生成される
* gcloud auth application-default login

## クラスタの診断

``` bash
kubectl get componentstatuses
```

## クラスタ上の全ノードの表示

``` bash
kubectl get nodes
```

## クラスタのノード数の変更

``` bash
gcloud container clusters resize [CLUSTER_NAME] --node-pool=[NODE_POOL] --size=[SIZE]
```

https://cloud.google.com/kubernetes-engine/docs/how-to/resizing-a-container-cluster

## クラスタの削除

``` bash
gcloud container clusters delete [CLUSTER_NAME]
```

https://cloud.google.com/kubernetes-engine/docs/how-to/deleting-a-container-cluster

## クラスタ上の全ノードの表示

``` bash
kubectl get pods
```

## ポッド名一覧の取得

``` bash
kubectl get pods -o jsonpath --template='{.items[*].metadata.name}'
```

## 参考

* [クイックスタート](https://cloud.google.com/kubernetes-engine/docs/quickstart)
