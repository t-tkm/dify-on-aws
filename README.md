# Dify on AWS with CDK(Frugal)
## はじめに
[こちらの記事](https://note.com/yukkie1114/n/n0d9c5551569f)
で紹介されているDifyのAWSへのデプロイ方法をカスタマイズしたものになります。

オリジナルのGitHubプロジェクトは[こちら](https://github.com/aws-samples/dify-self-hosted-on-aws)です。

## カスタマイズ後の利用方法
※事前準備などは、オリジナルの記事を参照してください。

- 起動(最小リソース)
    ```
    NAT_GATEWAY_COUNT=1 DESIRED_TASK_COUNT=1 cdk deploy
    ```
    ※今回はAZが2つであるため、作成可能なNAT Gatewayも2つまでとなります。
    従って、NAT_GATEWAY_COUNTの値を2以上に設定した場合、作成されるNAT Gateway
    は2つとなります。

- 停止
    ```
    NAT_GATEWAY_COUNT=0 DESIRED_TASK_COUNT=0 cdk deploy
    ```

