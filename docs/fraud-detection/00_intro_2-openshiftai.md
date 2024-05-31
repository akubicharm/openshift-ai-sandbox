---
layout: default
title: ワークショップの概要
nav_order: 2
---

# 全体像

このワークショップでは、OpenShift AIのサンドボックスを利用してOpenShift AIの機能を使っていきます。

![](../../assets/overview.png){: .d-block}


OpenShift AIを構成するコンポーネントは以下のとおりです。

* ワークベンチーJupyterNotebookなどを活用したモデルの開発環境
* データコネクションーモデルを保持するオブジェクトストレージへの接続情報
* パイプラインサーバーMLOpsのパイプラインを実行するサーバ
* Model Servingーモデルを公開するサーバ。APIで外部からアクセス可能。