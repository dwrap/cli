# dwrap

## 概要

`dwrap` is `Docker Wrapper`.
alpineベースのDockerコンテナを動的に生成して指定のコマンドを実行します。

## 使い方
 
```bash:dwrapの使い方

# alpineベースのコンテナを生成し、そこでcurlコマンドを実行
$ dwrap curl --help 

# jqコマンドを実行、入力としてjsonファイルをパイプで渡す
$ cat samples/jq.json | dwrap jq "."

```

## インストール

[リリースページ](https://github.com/dwrap/cli/releases/latest)から各プラットフォームごとにバイナリをダウンロードして展開してください。

## 内部動作

1) alpineをベースイメージに指定するDockerfileを準備
2) 指定のコマンドをapkコマンドでインストール
3) コンテナのentrypointを指定のコマンドに設定

# License

This project is published under [Apache 2.0 License](LICENSE).

# Author

* Kazumichi Yamamoto ([@yamamoto-febc](https://github.com/yamamoto-febc))
