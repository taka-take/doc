# 今日のレジュメ

## 利用技術

- Node.js
- Git
- React
- Redux
- Material UI
- WebAPI

## Node.js

- インストール方法
- バージョン管理ツールの話
- パッケージマネージャー（npm, yarn）

## Git

- インストール方法
- ローカルでの利用
  - git init
  - ステージング
  - コミット
  - .gitignore
- リモートリポジトリの利用
  - Github にアカウントを作る
  - SSH Key を登録する
  - リポジトリを作る
  - git clone する
  - コードを変更する
  - ステージングする
  - コミットする
  - プッシュする
- リモートリポジトリの確認
  - git remote -v
- リモートリポジトリの追加
  - git remote add origin url
- ブランチの作成
- プルリクエストの作成

## React

- JSX
  - jsの拡張構文
  - 直接HTMLのタグを書くことができる
- Component
  - JSXのタグを返す
  - class component
  - functional component
    - 記述が少なくて済む
    - lifesycle methodとstate を持つことができない
      - 16.8でリリースされるReact Hooksで改善（2月6日時点では16.7）
- props
  - パラメーターの引き渡しに利用
- State
  - パラメーターを保持するためのもの

### 補足1

- [Babel][4]
- [webpack][3]

## Redux

- Store
  - 値を保持する巨大なJSONの塊
- Action
  - Storeに対して変更を加えたい場合に発行する
  - 後述するReducerがActionを検知すると、storeの値が更新される
- Reducer
  - storeの値とactionを受け取って、storeに新しい値を設定する
  - Reducerには副作用を生む処理を書いてはいけない
    - 同じ入力に対して確率的に結果が変化する処理
    - 遅延処理
    - HTTPリクエスト処理

### 補足2

- react-redux
  - ReactとReduxを繋ぐためのconnect関数を提供
  - connect関数の書き方
- redux-thunk
  - reduxのactionで非同期処理を書けるようにするためのもの
- componentsとcontainers
  - componentsには純粋なComponentを格納
  - containersにはReduxに接続されたComponentを格納
- ReduxDevTool
  - Chromeの拡張
  - デバッグ実行の際にStoreの中身を見ることができる
- React / Redux による開発手順の例
  1. component を書く
  2. store に initialState を書く
  3. actionType を書く
  4. actionを書く
  5. reducer を書く
  6. component にイベントハンドラを書く

## Material UI

- Googleが提唱するデザインの型である「マテリアルデザイン」実現するCSSフレームワーク
- インストール方法
- 利用方法

## Web API

- URLアクセスすることで、サーバーの情報を取得したり、書き換えたりするもの
- 主にjson形式のデータでやり取りを行う
- 今回は以下の書籍とサイトを参考にC#で実装
  - [参考１][1]
  - [参考２][2]
  
## 環境構築

- プロジェクトテンプレートのダウンロード
- テンプレートの構成
- パッケージの更新

[1]:https://www.oreilly.co.jp/books/9784873116860/
[2]:https://tahirnaushad.com/2017/08/31/creating-crud-api-in-asp-net-core-2-0/
[3]:https://webpack.js.org/
[4]:https://babeljs.io/
