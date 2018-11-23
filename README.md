# ネコミミでもわかるフロントエンド開発環境構築

## 第1章 まずは準備から

### yarnをインストールする

```
$ brew install yarn
```

### package.jsonを作成する

```
$ yarn init
```

## 第2章　JavaScriptを動かす

### Babelモジュールを追加する

```
$ yarn add --dev @babel/preset-env
```

### webpackモジュールを追加する

```
$ yarn add --dev webpack webpack-cli @babel/core babel-loader
```

### JavaScriptをビルドする

```
$ yarn build:dev
```

### JavaScriptを実行する

```
$ node ./dist/index.bundle.js
```

### webpack-dev-serverモジュールを追加する

```
$ yarn add --dev webpack-dev-server html-webpack-plugin
```

`html-webpack-plugin`は開発サーバー用にHTMLを自動的に出力するプラグイン。

### 開発用サーバーを立ち上げる

```
$ yarn serve
```

## 第3章 JavaScriptのためのパワフルなツール

### eslint-config-airbnbが指定するバージョンを調べる

```
$ yarn info eslint-config-airbnb peerDependencies
yarn info v1.12.3
{ eslint:
   '^4.19.1 || ^5.3.0',
  'eslint-plugin-import':
   '^2.14.0',
  'eslint-plugin-jsx-a11y':
   '^6.1.1',
  'eslint-plugin-react':
   '^7.11.0' }
✨  Done in 0.31s.
```

### ESLintモジュールを追加する

```
yarn add --dev eslint-config-airbnb \
eslint@^5.3.0 \
eslint-plugin-import@^2.14.0 \
eslint-plugin-jsx-a11y@^6.1.1 \
eslint-plugin-react@^7.11.0 \
babel-eslint
```
