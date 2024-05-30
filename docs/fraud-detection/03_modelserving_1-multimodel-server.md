---
layout: default
title: マルチモデルサーバのデプロイ
nav_order: 8
---

# マルチモデルサーバのデプロイ

## ワークベンチの停止

Sandbox環境はリソースが少ないので、省エネのためにワークベンチを停止します。


1. ワークベンチの一覧でStatusのトグルボタンをクリックしてワークベンチを停止します。
![](../../assets/oai_stop_workbench.png){: .d-block}
![](../../assets/oai_stop_workbench_2.png){: width="400" .d-block}


## モデルサーバのデプロイ
{:style="counter-reset:none"}
1.「Models」タブを表示し「Add model server」ボタンをクリックします。
![](../../assets/oai_add_modelserver_1.png){: .d-block}

{: .note }右上の緑の四角で囲んだところに「Multi-model serving enabled」と表示されているので、この環境ではMulti-modelサービングだけが利用可能です。

1. Add model serverダイアログでパラメータを入力して、画面下部の「Add」ボタンをクリックします。
* モデルサーバ名とランタイムの設定
<dl>
<dt>Model server name</dt><dd>Model Server</dd>
<dt>Serving runtime</dt><dd>OpenVINO Model Server</dd>
</dl>
![](../../assets/oai_add_modelserver_runtime.png){: .d-block}
* モデルサーバのレプリカ数の設定
<dl>
<dt>Number of model server replicas to deploy</dt><dd>1</dd>
</dl>
![](../../assets/oai_add_modelserver_replicas.png){: .d-block}
* モデルサーバのサイズとアクセラレータの設定。
<dl>
<dt>Model server site</dt><dd>small</dd>
<dt>Accelerator</dt><dd>None (GPUを使わない)</dd>
</dl>
![](../../assets/oai_add_modelserver_size.png){: .d-block}
* 外部からアクセスするためのRouteを公開するかどうかの設定
<dl>
<dt>Make deployment models available throught an external route</dt><dd>チェックする</dd>
<dt>Reuire token authenticatino</dt><dd>チェックする</dd>
</dl>
![](../../assets/oai_add_modelserver_route.png){: .d-block}
* 全部入力が終わったら「Add」ボタンをクリック
![](../../assets/oai_add_modelserver_add.png){: .d-block}

## モデルのデプロイ

{:style="counter-reset:none"}
1. デプロイしたモデルサーバ名の行にある「Deploy model」ボタンをクリックします。
![](../../assets/oai_model_deploy_model_1.png){: .d-block}


1. パラメータを入力したら、画面下部の「Deploy」ボタンをクリックします。
* モデル名を設定
<dl>
 <dt>Model name</dt><dd>fraud</dd>
</dl>
![](../../assets/oai_model_deploy_model_name.png){: .d-block}
* モデルフレームワークを設定
<dl>
 <dt>Model framework</dt><dd>onnx - 1</dd>
</dl>
![](../../assets/oai_model_deploy_model_framework.png){: .d-block}
* モデルが保存されているオブジェクトストレージを設定
<dl>
 <dt>Name</dt><dd>My Storage</dd>
 <dt>Path</dt><dd>/models/fruad/1</dd>
</dl>
![](../../assets/oai_model_deploy_model_path.png){: .d-block}
* 全部入力したら「Deploy」ボタンをクリック
![](../../assets/oai_model_deploy_model_button.png){: .d-block}


1. モデルデプロイのステータスを確認
![](../../assets/oai_model_deploy_model_verify.png){: .d-block}