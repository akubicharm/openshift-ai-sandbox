---
layout: default
title: Jupyter notebookの利用
nav_order: 6
---

# Jupyter notebookの利用

Notebookを起動して、サンプルのアプリケーションをgit cloneしてモデルを開発する準備をします。

![](../../assets/overview_notebook.png)

1. Jupyter notebookにブラウザで開いていない場合は、ワークベンチを選択し「Open」のリンクをクリックします。
![](../../assets/oai_create_workbench_open.png){: .d-block}

1. OpenShiftのログインダイアログが表示された場合は、「DevSandBox」ボタンをクリックしてログインします。
![](../../assets/oai_notebook_login.png){: width="400" .d-block}

1. Notebookが開いたら、左上のGitのアイコンをクリックします。
![](../../assets/oai_notebook_git.png){: .d-block}

1. サンプルのGitリポジトリのURLをコピペして「Clone」ボタンをクリックします。
```text
https://github.com/rh-aiservices-bu/fraud-detection.git
```
![](../../assets/oai_notebook_clone.png){: width="400" .d-block}

1. Cloneした fraud-detectionのディレクトリをクリックして、ソースコードの一覧を確認します。
![](../../assets/oai_notebook_verify_clone.png){: width="400" .d-block}
![](../../assets/oai_notebook_list_dir.png){: width="400" .d-block}


[Prev](./02_wb_1-workbench.html){: .float-left}
[Next](./02_wb_3-train-and-save-model.html){: .float-right}