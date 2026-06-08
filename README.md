# study-git
gitのお勉強

* [公式が公開している日本語の説明書](https://git-scm.com/book/ja/v2)

## コマンドラインインターフェース（CLI:Command Line Interface）

### リポジトリの作成と管理対象の登録
ディレクトリexampleを丸ごとリポジトリとして登録する。

ディレクトリexampleをカレントディレクトリにして
```
$ git init
```
これで、ディレクトリexample直下に

- .git

というディレクトリができる。
これが履歴情報を保存するディレクトリとなる。
ただ、この初期状態はディレクトリexample下のどのファイルも変更を追跡しない。
ディレクトリexample下の全てのファイル(.gitディレクトリは除外される)を追跡対象にするには
```
$ git add .
```
とする。

#### 特定ファイルの追跡指定
例えばディレクトリexampleの構成が以下とする。
```
example/
  a/
    a.txt
  b/
    b.txt
  c.txt
```
このうちa/a.txtだけ追跡したいなら
```
git add a/a.txt
```
とする。

### README.mdで使うMarkdown言語について

* [目次の用意](https://qiita.com/eyuta/items/b1a53f3da8c5f8e7f41d)
