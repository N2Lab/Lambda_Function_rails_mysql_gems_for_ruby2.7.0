# What's this
Lambda_Function_rails_mysql_gems_for_ruby2.7.0 は AWS Lambda カスタムランタイム Ruby2.7.0 Layer 上で起動する
Mysql利用Rails6.0.2.2 の Lambda functionテンプレートです。

# TODO
  "errorMessage": "libyaml-0.so.2: cannot open shared object file: No such file or directory - /opt/ruby/lib/ruby/2.7.0/x86_64-linux/psych.so",


# AWS Lambda デプロイ手順
```
$ vi lambda_function.rb
(LambdaHandler開発)
$ vi Gemfile
(Gemfile 修正)
$ bundle install --path vendor/bundle
$ zip -r function.zip lambda_function.rb vendor Gemfile Gemfile.lock 
$ aws lambda update-function-code --function-name rubyGemTest2--zip-file fileb://function.zip
```
