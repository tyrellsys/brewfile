homebrew/Brew Bundle用 Brewfileテンプレート
===

OSX初期セットアップテンプレートです

- [homebrew](http://brew.sh/index_ja.html)
- [homebrew/bundle](https://github.com/Homebrew/homebrew-bundle)
- [homebrew/cask](http://caskroom.io/)

## インストール手順

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

## TODO

- インストールパッケージの精査

### phpbrew

利用する場合は以下をコマンドで実行しておく

```bash
brew link curl --force
brew link icu4c --force
brew link libxml2 --force
brew link openssl --force
```

インストールや設定参考url  
http://www.karakaram.com/mac-install-phpbrew
