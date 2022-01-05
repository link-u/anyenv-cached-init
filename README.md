# anyenv-cached-init

## 1. TOC

<!-- TOC depthFrom:2 -->

- [1. TOC](#1-toc)
- [2. About](#2-about)
- [3. Installation](#3-installation)
- [4. Usage](#4-usage)
- [5. License](#5-license)

<!-- /TOC -->

<br>

## 2. About

**English**

This is an [anyenv](https://github.com/anyenv/anyenv) plugin to tuing performance for `anyenv init --no-rehash -`.

This plugin store the initialization script created by `anyenv init --no-rehash -` as a cached file.
If this cache file exists, it will be read.

Also if there is an update to `anyenv` or `**env`, the cache file will be recreated.

<br>

**Japanese**

これは `anyenv init --no-rehash -` を高速化するための anyenv 用のプラグインです.

`anyenv init --no-rehash -` によって作られる初期化用スクリプトが [cached](./cached/) ディレクトリにキャッシュファイルとして保存されます.
キャッシュファイルが存在すればそれを読み込みます.

もし anyenv や **env に更新があればキャッシュファイルは再作成されます.

<br>

## 3. Installation

```
mkdir -p $(anyenv root)/plugins \
    && git clone https://github.com/link-u/anyenv-cached-init.git $(anyenv root)/plugins/anyenv-cached-init
```

<br>

## 4. Usage

**English**

Rewrite `eval "$(anyenv init --no-rehash -)"` in your `~/.zshrc` or `~/.bashrc` to `source "$(anyenv cached-init)"`

<br>

**Japanese**

`~/.zshrc` もしくは `~/.bashrc` の `eval "$(anyenv init --no-rehash -)"` を `source "$(anyenv cached-init)"` に書き換えてください.

<br>

## 5. License

[MIT](./LICENSE.md)
