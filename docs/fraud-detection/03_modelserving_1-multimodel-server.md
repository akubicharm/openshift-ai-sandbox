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

1.「Models」タブを表示し「Add model server」ボタンをクリックします。
![](../../assets/oai_add_modelserver_1.png)

{: .note }右上の緑の四角で囲んだところに「Multi-model serving enabled」と表示されているので、この環境ではMulti-modelサービングだけが利用可能です。


1. Add model serverダイアログでパラメータを入力して、画面下部の「Add」ボタンをクリックします。
{: .d-block}
![](../../assets/oai_add_modelserver_runtime.png)
{: .d-block}
Model server name:Model Server
Serving runtime:OpenVINO Model Server
{: .d-block}
![](../../assets/oai_add_modelserver_replicas.png)
{: .d-block}
Number of model server replicas to deploy: 1
{: .d-block}
![](../../assets/oai_add_modelserver_size.png)
{: .d-block}
Model server site: small
Accelerator: None
{: .d-block}
![](../../assets/oai_add_modelserver_route.png)
{: .d-block}
Make deployment models available throught an external route: チェックする
Reuire token authenticatino: チェックする
{: .d-block}
![](../../assets/oai_add_modelserver_add.png)
{: .d-block}
全部入力が終わったら「Add」ボタンをクリックします。





