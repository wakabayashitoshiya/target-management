# target-management

目標管理用のリポジトリ

## 要約

要約ってほどのことは無いが、目標管理のネタ  
今回はReact.jsを使用してなにかを作るらしいので公開するにはかなりイケてないがアップします。  
（なにかの役に立てばよいが・・・）、あと間違ってたらすいません。

## 用意するもの

* wsl(ubuntu) あるといいなー
* vscode
* Node.js
* yarn or npm
* etc

※ 順繰り書いていきます。

## 実行前の準備

詳しい手順は自身で調べてください。

* 用意するものを用意ｗだね。  
* wsl(ubuntu)にGit,Node.js,yarn or npmをインストール  
* vscodeにはJS・Reactに必要な拡張機能をインストールしておく
* Live Serverは便利なので入れておこう

※ ここも順繰り書いていきます。

## 実行方法

キチンと必要なものがインストール・設定がされていれば動くはず

Gitでclone作成後に該当ディレクトリで以下を実行

```shell
yarn install
または 
npm install
```

まずはこれでコンパイル・実行に必要な```node_module```がカレントディレクトリに  
ダウンロードされてきます。

すでに```package.json```にscriptが埋め込まれているので、まずは

```shell
yarn run dev
または
yarn dev
または
npm run dev
```

入力して実行すると、```src```以下のソースがコンパイルとバンドルされ```dist```に```bundle.js```が作成されます。

※ この辺の設定は```webpack.config.js```に記載してあります。
なにかの参考にしてください。

この状態で```src```以下のソースが監視対象となり、ファイルを変更するたびにコンパイル・バンドルが実行されます。

vscodeにインストールしたLive Serverを起動して組み合わせることにより、リアルタイムで変更内容がブラウザに反映されます。  
なんですが、、、サーバサイド通信もテストでいれてしまったので、こちらで試して見てください。

```shell
yarn run start
または
yarn start
または
npm run start
```

```webpack-dev-server```を使用しております。  
勝手にブラウザが立ち上がってくるかと思います。  

※ ここも順繰り書いていきます。(またこれかｗ)

## 解説など

React Hooksをメインに使って行きます。  
サーバサイド通信もテストで入れたので、サーバサイドのロジックも合わせて導入しようかと思ってます。  

ここも追って追記します。

## その他

今回は、なんとなくゼロからの構築みたいになっているが公式にいろいろな  
ツールチェインがあると書いてあるので、試してみるのもありですね。  
<https://ja.reactjs.org/docs/create-a-new-react-app.html#create-react-app>

ESLint(静的解析ツール)を導入してしまったため、変な書き方にするとエラーになるかもよ。  
ESLint ルール 一覧 (日本語)  
<https://garafu.blogspot.com/2017/02/eslint-rules-jp.html>

多少縛りがきついほうが、きれいにかけるかもよ。
ルールは後見直してみます。  
