# go-cli-hello-world

Goで"Hello World!"+αを表示するだけのCLIツール。

## Installation

[Releases](https://github.com/NakuRei/go-cli-hello-world/releases)から各プラットフォームに対応したバイナリファイルをダウンロードして実行してください。

## Usage

`go-cli-hello-world`コマンドを実行すると、"Hello World!"が表示されます。

```shell
$ go-cli-hello-world
Hello World!
```

"Hello"の部分は`--greeting`あるいは`-g`フラグで変更できます。

```shell
$ go-cli-hello-world -g Hi
Hi World!
$ go-cli-hello-world --greeting Hi
Hi World!
```

サブコマンド`hi`が実装されています。実行すると"Hello World!"の代わりに"(〃'▽'〃)ﾉおはよー"が表示されます。

```shell
$ go-cli-hello-world hi
(〃'▽'〃)ﾉおはよー
```

バージョン情報は`--version`フラグで表示できます。

```shell
$ go-cli-hello-world --version
# あるいは
$ go-cli-hello-world hi --version
```

説明文を`-h`フラグで表示できます。

```shell
$ go-cli-hello-world -h
# あるいは
$ go-cli-hello-world hi -h
```

## Development

### Requirement

- Docker version 24.0.5

### Using packages

- [cobra-cli](https://github.com/spf13/cobra-cli)
- [Staticcheck](https://staticcheck.dev/)
- [GoReleaser](https://goreleaser.com/)

```shell
RUN go install github.com/spf13/cobra-cli@v1.3.0
RUN go install honnef.co/go/tools/cmd/staticcheck@latest
RUN go install github.com/goreleaser/goreleaser@latest
```

## Author

NakuRei

- [misskey.systems](https://misskey.systems/@nakurei7901)
- [X](https://twitter.com/nakurei7901)

## License

[MIT License](https://github.com/NakuRei/go-cli-hello-world/blob/main/LICENSE)
