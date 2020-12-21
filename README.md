# aws-alarm

## 概要

- CIS Amazon Web Service Foundations BenchmarkというAWSのセキュリティガイドラインがある
- このセキュリティガイドラインのうち、`3.Monitoring`を満たすようなアラームを作成した

## 使い方

- SystemManagerのパラメータストアにアラームの通知先のemailアドレスを登録しておく
  - パラメータ名を`SecurityAlarmEmailAddress`とする
- 以下のコマンドを打つ(変更セットの作成)
    
    `$ ./create-change-set.sh`

- 変更セットを確認した後、以下のコマンドを打つ(実際にデプロイする)
  
    `$ ./create-change-set.sh deploy`

## 参考 URL

- [AWS を使うときに確認すべき 52 のセキュリティチェック項目と 15 分でできる簡単なチェックの方法](https://dev.classmethod.jp/articles/aws-security-check/)
- [AWS CloudTrail（2）CIS AWS Foundations Benchmark に準拠するための通知設定](http://tech.blog.surbiton.jp/aws-cloudtrail-3-cloudwatch-alarm-sns-notification/)
- [AWS_CIS_Foundatins_Bentchmark.pdf](https://d0.awsstatic.com/whitepapers/compliance/AWS_CIS_Foundations_Benchmark.pdf)
