---
layout: default
title: モデルのAPI呼び出し
nav_order: 9
---

# モデルの　API呼び出し

OpenShiftのRouteで外部向けに公開されたAPIを呼び出します。


## Bearer トークンの取得

API呼び出し時のトークン認証を有効にしているので、トークンを取得します。

1. OpenShiftコンソールを開きます。

1. OpenShiftコンソールの右上の「ログインコマンドのコピー」を選択してトークンをコピーします
![](../../assets/ocp_copy_token.png){: .d-block}


## モデルのAPI呼び出し

1. OpenShift AIのコンソールでModel Servingタブを表示して、Model ServerのURLをコピーします。
![](../../assets/oai_copy_model_api_url.png){: .d-block}
URLはこういう形式になっています。
```
https://fraud-[RH_developerのアカウント名]-dev.apps.sandbox-m4.g2pi.p1.openshiftapps.com/v2/models/fraud/infer
```


1. curlコマンドでAPIを呼び出します。
Model ServerのURL、Bearerトークンは各自の環境に合わせて編集してください。
```
curl -X POST -H "Content-Type: application/json" \
-H "Authorization: Bearer sha256~xxxxx0_VDZxx0xxxAUxPAFJxxEFxxxSxVxxUOXxE00x" \
-d '{"inputs": [{"name": "dense_input","shape": [1, 5],"datatype": "FP32","data": [0.3111400080477545, 1.9459399775518593, 1.0, 0.0, 0.0]} ]}' \
https://fraud-my-user-name-dev.apps.sandbox-m4.g2pi.p1.openshiftapps.com/v2/models/fraud/infer
```
VSCodeのREST Clientを利用する場合
```
###
POST https://fraud-kay-akubichan-dev-dev.apps.sandbox-m4.g2pi.p1.openshiftapps.com/v2/models/fraud/infer
Content-type: application/json
Authorization: Bearer sha256~qskfh5_VDZtk5cllAUePAFJsqEFjebSiVjnUOXqE99k

{
  "inputs": [
    {
      "name": "dense_input",
      "shape": [1, 5],
      "datatype": "FP32",
      "data": [0.3111400080477545, 1.9459399775518593, 1.0, 0.0, 0.0]
    } 
  ] 
}
```


