# AWS SDK for C++ Container

AWS SDK for C++ ビルド＆インストール
```
docker image build -t  aws-sdk-cpp-s3:latest -f Dockerfile_SDK .
```

S3アクセスサンプルアプリをビルド
```
docker image build -t s3-sample -f Dockerfile_AP .
```

実行
```
docker container run --rm \
    --name s3-sample \
    --env AWS_ACCESS_KEY_ID=XXXX \
    --env AWS_SECRET_ACCESS_KEY=XXXX \
    --env AWS_DEFAULT_REGION=ap-northeast-1 \
    s3-sample
```

