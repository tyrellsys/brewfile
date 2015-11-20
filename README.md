homebrew/Brew Bundle用 Brewfileテンプレート
===

OSX初期セットアップテンプレートです

- [homebrew](http://brew.sh/index_ja.html)
- [homebrew/bundle](https://github.com/Homebrew/homebrew-bundle)
- [homebrew/cask](http://caskroom.io/)

## インストール手順
- 先にXcode Command Line Developer Toolsをインストールしといてください  
```
xcode-select --install
```
- このレポジトリを自分のアカウントにForkしてください
- Forkしたレポジトリを適当なところにダウンロードします
- Brewfileを必要に応じてコメントアウトしたり、追加してください
  - 事前に[homebrew/cask](http://caskroom.io/)をインストールしておくと  
    ```
    brew cask search hogehoe
    ```  
    で探すのに便利です。
- App StoreからXcodeをダウンロードしたあとライセンス認証を行う
- homebrewをターミナルからインストールする
- homebrew/bundleもインストールします
- Brewfileのあるディレクトリで  
  ```
  brew bundle
  ```  
  と打つとインストールが始まります。
- 編集したファイルはコミットしてプッシュしておけば、自分好みのBrewfileができます

## モジュール別注意点

### phpenv

- .bashrcに以下を追加する  
```
export PATH=$PATH:~/.phpenv/bin
eval "$(phpenv init -)"
```
- phpenvが見つからない時は以下シェルを実行する
```
/usr/local/bin/phpenv-install.sh
```
- php-buildする（例）  
```
php-build 5.6.15 ~/.phpenv/versions/5.6.15
```
- phpenvで切り替える  
とりあえず  
```
phpenv rehash
```  
次にインストールされているバージョンを確認  
```  
phpenv versions
```  
使いたいバージョンを指定する  
```
phpenv global 5.6.15
php -v
```  
```
Copyright (c) 1997-2015 The PHP Group
Zend Engine v2.6.0, Copyright (c) 1998-2015 Zend Technologies
    with Zend OPcache v7.0.6-dev, Copyright (c) 1999-2015, by Zend Technologies
    with Xdebug v2.3.3, Copyright (c) 2002-2015, by Derick Rethans
```



## TODO

- インストールパッケージの精査
