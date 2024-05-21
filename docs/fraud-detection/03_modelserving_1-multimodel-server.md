---
layout: default
title: マルチモデルサーバのデプロイ
nav_order: 8
---

# マルチモデルサーバのデプロイ

## ワークベンチの停止

Sandbox環境はリソースが少ないので、省エネのためにワークベンチを停止します。

{:style="counter-reset:none"}
1. ワークベンチの一覧でStatusのトグルボタンをクリックしてワークベンチを停止します。
{: .d-block}
![](../../assets/oai_stop_workbench.png)
![](../../assets/oai_stop_workbench_2.png)


##　モデルサーバのデプロイ

1.「Models」タブを表示し「Add model server」ボタンをクリックします。
![](../../assets/oai_add_modelserver_1.png)


{: .note }右上の緑の四角で囲んだところに「Multi-model serving enabled」と表示されているので、この環境ではMulti-modelサービングだけが利用可能です。


1. Add model serverダイアログでパラメータを入力して、画面下部の「Add」ボタンをクリックします。

* モデルサーバ名とランタイムの設定
{: .d-block}
Model server name:Model Server
Serving runtime:OpenVINO Model Server
{: .d-block}
![](../../assets/oai_add_modelserver_runtime.png)
{: .d-block}

* モデルサーバのレプリカ数の設定
Number of model server replicas to deploy: 1
{: .d-block}
![](../../assets/oai_add_modelserver_replicas.png)

* モデルサーバのサイズとアクセラレータの設定。
{: .d-block}
Model server site: small
Accelerator: None (GPUを使わない)
{: .d-block}
![](../../assets/oai_add_modelserver_size.png)

* 外部からアクセスするためのRouteを公開するかどうかの設定
{: .d-block}
Make deployment models available throught an external route: チェックする
Reuire token authenticatino: チェックする
{: .d-block}
![](../../assets/oai_add_modelserver_route.png)


* 全部入力が終わったら「Add」ボタンをクリック
{: .d-block}
![](../../assets/oai_add_modelserver_add.png)


##　モデルのデプロイ

{:style="counter-reset:none"}
1. デプロイしたモデルサーバ名の行にある「Deploy model」ボタンをクリックします。
{: .d-block}
![](../../assets/oai_model_deploy_model_1.png)


1. パラメータを入力したら、画面下部の「Deploy」ボタンをクリックします。

* モデル名を設定
Model name: fraud
{: .d-block}
![](../../assets/oai_model_deploy_model_name.png)

* モデルフレームワークを設定
Model framework : onnx - 1
{: .d-block}
![](../../assets/oai_model_deploy_model_framework.png)

* モデルが保存されているオブジェクトストレージを設定
Name: My Storage
Path: /models/fruad/1
{: .d-block}
![](../../assets/oai_model_deploy_model_path.png)

* 全部入力したら「Deploy」ボタンをクリック
{: .d-block}
![](../../assets/oai_model_deploy_model_button.png)


1. モデルデプロイのステータスを確認
{: .d-block}
![](../../assets/oai_model_deploy_model_verify.png)