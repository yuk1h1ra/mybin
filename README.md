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

## hugo-new-post

[blog-with-hugo](https://github.com/yuk1h1ra/blog-with-hugo)では、ブログ記事を`posts/:year/:month/article`になるようにしている。そのため、新しくブログ記事を作成する際のタイプ量を減らすhugoのラッパーコマンドである。

Example:
```bash
$ hugo-new-post article-title
/home/yuk1h1ra/[directories]/blog-with-hugo/content/posts/2020/11/article-title/index.md created
```

## mp42mov

フリー版のLinux用DaVinci Resolveで発生する、mp4コンテナとAAC音声がサポートされていないため、[Arch Wiki](https://wiki.archlinux.jp/index.php/DaVinci_Resolve#.mp4_.E3.82.AF.E3.83.AA.E3.83.83.E3.83.97.E3.81.8C.E9.9F.B3.E5.A3.B0.E3.82.AF.E3.83.AA.E3.83.83.E3.83.97.E3.81.A8.E3.81.97.E3.81.A6.E8.AA.8D.E8.AD.98.E3.81.95.E3.82.8C.E3.82.8B.E3.81.AE.E3.81.AB.E9.9F.B3.E5.A3.B0.E3.81.8C.E5.87.BA.E5.8A.9B.E3.81.95.E3.82.8C.E3.81.AA.E3.81.84)に記載されているように、mp4ファイルをmovフォーマットに変換するコマンド

Example:
```bash
$ mp42mov video.mp4
```

## mov2mp4

Googleから推奨される[アップロードエンコーディング設定](https://support.google.com/youtube/answer/1722171?hl=ja)に準拠するため、DaVinci Resolveで書き出しをしたmovファイルをmp4フォーマットに変換するコマンド

Example:
```bash
$ mov2mp4 render.mov
```