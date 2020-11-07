# mybin

## Description

.bashrc/.zshrcなどに記述していたスクリプト群を一元管理したいというモチベーションからこのリポジトリを作成。
基本的にはオレオレスクリプトなので、README通りにしたけど動かないや、追加機能の対応などはしない方針。
必要だと思った機能を思いついたときに更新していく。

## Set up

## このリポジトリにpathを通す

mybinのあるディレクトリ構造を確認する。

```bash
$ pwd
/home/yuk1h1ra/[repositories]/mybin
```

[Prezto](https://github.com/sorin-ionescu/prezto)を使用しているため、`~/.zprofile`のpath部分に追記する

```.zprofile
(中略)
# Set the list of directories that Zsh searches for programs.
path=(
  /usr/local/{bin,sbin}
  /home/yuk1h1ra/[repositories]/mybina
  $path
)
(中略)
```

## Commands

### hugo-new-post

[blog-with-hugo](https://github.com/yuk1h1ra/blog-with-hugo)では、ブログ記事を`posts/:year/:month/article`になるようにしている。そのため、新しくブログ記事を作成する際のタイプ量を減らすhugoのラッパーコマンドである。

Example:
```bash
$ hugo-new-post article-title
/home/yuk1h1ra/[directories]/blog-with-hugo/content/posts/2020/11/article-title/index.md created
```
