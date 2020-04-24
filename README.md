# What's this
Lambda_Layer_ruby2.7.0 は AWS Lambda カスタムランタイム用の Ruby2.7.0 Layer用ライブラリです。
下記「AWS Lambda デプロイ手順」によりAWS Lambda Layerにデプロイ可能です。
詳細 https://n2lab.hatenablog.com/entry/2020/04/11/190541#docker-build--rails%E3%82%B5%E3%83%BC%E3%83%90%E8%B5%B7%E5%8B%95

# AWS Lambda デプロイ手順
```
$ zip -r ruby_270_layer.zip bootstrap lib ruby
$ aws lambda publish-layer-version     --layer-name ruby_270     --description "Ruby 2.7.0"     --compatible-runtimes provided     --license-info MIT     --zip-file fileb://ruby_270_layer.zip
```
