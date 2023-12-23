# イメージをローカルでテスト

```
イメージのビルド
docker build --platform linux/amd64 -t smart-morning-batch:test .

コンテナの起動
docker run --platform linux/amd64 -p 9000:8080 smart-morning-batch:test

イベントをローカルエンドポイントにポスト
Invoke-WebRequest -Uri "http://localhost:9000/2015-03-31/functions/function/invocations" -Method Post -Body '{}' -ContentType "application/json"
```
