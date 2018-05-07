# GKE

## クラスタの作成

``` bash
gcloud container clusters create <クラスタ名>
```

## クラスタ利用の認証情報の取得

> どっちをやればいいんだろう?

* gcloud container clusters get-credentials <クラスタ名>
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

## 参考

* [クイックスタート](https://cloud.google.com/kubernetes-engine/docs/quickstart)
