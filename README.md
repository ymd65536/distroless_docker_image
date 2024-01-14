# distroless_docker_image

distrolessのイメージでコンテナを作成してみた

## セットアップ

```bash
gh repo clone ymd65536/distroless_docker_image
```

## 実行手順

distrolessディレクトリに移動して`docker build`を実行します。

```bash
cd distroless
docker build -t test_distroless:1 .
docker run -it --rm test_distroless:1
```

alpineディレクトリに移動して`docker build`を実行します。

```bash
cd alpine
docker build -t test_alpine:1 .
```

## イメージサイズを比較

以下のコマンドを実行すると、イメージサイズを確認できます。

```bash
docker images
```

実行結果

```text
REPOSITORY                           TAG          IMAGE ID       CREATED         SIZE
test_alpine                          1            374875ee50bb   8 seconds ago   333MB
test_distroless                      1            e6ee09fc6a8e   2 minutes ago   132MB
```
