# Lambda_Layer_ruby2.7.0
read https://n2lab.hatenablog.com/entry/2020/04/11/190541#docker-build--rails%E3%82%B5%E3%83%BC%E3%83%90%E8%B5%B7%E5%8B%95

# deploy Ruby 2.7.0 layer 
```
$ zip -r ruby_270_layer.zip bootstrap lib ruby
$ aws lambda publish-layer-version     --layer-name ruby_270     --description "Ruby 2.7.0"     --compatible-runtimes provided     --license-info MIT     --zip-file fileb://ruby_270_layer.zip
```