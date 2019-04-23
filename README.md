## 懶人包 Cromwell on AWS Batch
![](https://docs.opendata.aws/genomics-workflows/orchestration/cromwell/images/cromwell-on-aws_infrastructure.png)

https://docs.opendata.aws/genomics-workflows/orchestration/cromwell/cromwell-overview/
1. 登入 AWS　後直接使用 `https://github.com/aws-samples/aws-genomics-workflows/blob/master/src/templates/cromwell/cromwell-aio.template.yaml` 做整個環境的部署
2. 部署大概要半個小時左右
3. 部署會用到 1 個新建的 VPC，如果原本帳號有多個 VPC 須注意
4. 建立一個合法的 S3 bucket 命名空間，這會放置 cromwell 的運算資料及結果
6. EC2 預先建立 key pair , 使用 cromwell terminal 會用到
