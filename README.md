# 職務経歴書

## 基本情報

|key|value|
|---|-----|
|Name|南 優也 (みなみ ゆうや)|
|Twitter|[@mooonyman](https://mobile.twitter.com/mooonyman)|
|GitHub|[yuya373 (Yuya Minami)](https://github.com/yuya373)|
|はてなブックマーク|[mooonymann](http://b.hatena.ne.jp/mooonymann/)|

## スキル

- Ruby (v1.9 ~ v2.x)
  - Ruby on Rails (v3 ~ v5)
- TypeScript
  - React
  - ReactNative
    - Expo(v33.0.3)
  - Redux
    - redux-thunk
- JavaScript
  - webpack (v1 ~ v4)
  - babel
  - React
  - react-router (v3 ~ v4)
  - Redux
    - redux-saga
  - Immutable.js
  - Electron
    - [yuya373/manga-viewer](https://github.com/yuya373/manga-viewer)
  - Chrome extension
    - [yuya373/memo](https://github.com/yuya373/memo)
- Scala (v2.11)
  - Finagle
  - Finch
  - TwitterServer
- Emacs Lisp
  - プラグイン
    - [yuya373/emacs-slack: slack client for emacs](https://github.com/yuya373/emacs-slack)
    - [yuya373/gh-viewer](https://github.com/yuya373/gh-viewer)
    - [yuya373/emacs-github-graphql-client](https://github.com/yuya373/emacs-github-graphql-client)
    - [yuya373/emacs-bq: emacs "bq" command interface](https://github.com/yuya373/emacs-bq)
- Swift
  - 実務経験なし
  - 公式チュートリアル + α
    - [yuya373/FoodTracker](https://github.com/yuya373/FoodTracker)
  - Dropboxに保存するメモ帳
    - [yuya373/Note](https://github.com/yuya373/Note)
- Rust
  - 実務経験なし
  - 本やチュートリアルの写経
    - [yuya373/programming-rust](https://github.com/yuya373/programming-rust)
    - [yuya373/trpl](https://github.com/yuya373/trpl)
    - [yuya373/line-chat](https://github.com/yuya373/line-chat)
    - [yuya373/rust_dns](https://github.com/yuya373/rust_dns)
- Unity, C#
  - 実務経験なし
  - チュートリアル
    - [yuya373/Roll-a-Ball](https://github.com/yuya373/Roll-a-Ball)
  - Oculus Go用のシューティングアプリ
    - [yuya373/VRShootingGame](https://github.com/yuya373/VRShootingGame)
- Go
  - 実務経験なし
  - [O'Reilly Japan - Go言語でつくるインタプリタ](https://www.oreilly.co.jp/books/9784873118222/)
    - [yuya373/concurrency](https://github.com/yuya373/concurrency)
  - [O'Reilly Japan - Go言語による並行処理](https://www.oreilly.co.jp/books/9784873118468/)
    - [yuya373/monkey](https://github.com/yuya373/monkey)

## 興味があるもの
- 静的型付き言語での開発
  - Rust
  - TypeScript
  - Swift
  - Go
  - Scala
- iOSアプリ開発
- ミドルウェア開発

## 職務経歴

### 2019/03 - : 株式会社maricuru
職務: ソフトウェアエンジニア
環境: Ruby(2.x), Ruby on Rails(5.x), Grape(0.19) MySQL(RDS), Redis(ElastiCache), ReactNative, Expo, Redux, ECS, Amazon Elastic Search Service

#### ReactNativeアプリの開発
- [結婚式準備の相談サイト【maricuru】](https://maricuru.com/pages/app/)のアプリ開発
  - 既存コードのTypeScript化
  - パフォーマンスチューニング
    - `PureComponent`, `react-redux`の`Connect`等を使って`render`回数を減らす
    - `requestAnimationFrame`での遅延レンダリング
    - カルーセルでのオンメモリ状態の画像を減らすことでのメモリ使用量の削減
  - `redux-thunk`を用いてコンポーネントから副作用のあるコードの分離

#### WebAPIの開発
- 上記アプリのAPI開発
- パフォーマンスチューニング
  - 遅いクエリの改善
    - index追加
    - クエリ自体の修正
  - n+1の修正
  - jbuilderから[procore/blueprinter](https://github.com/procore/blueprinter)への移行

#### インフラ環境の整備
- 既存インフラのterraform(0.11.11)化
- cronからECS Scheduled Tasksへの移行


### 2016/01 - 2019/02 : 株式会社Rebase
職務: Webアプリケーションエンジニア
環境: Ruby(2.x), Ruby on Rails(4.x), PostgreSQL(RDS), Redis(ElastiCache), Webpack, React, Redux, ECS, Scala(2.11), Finagle, Finch, Elastic Beanstalk, Amazon Elastic Search Service

#### Webアプリケーションの開発
- [貸し会議室・レンタルスペースの検索・予約なら | インスタベース](https://www.instabase.jp/)の開発
  - バックエンド
    - Ruby, Ruby on Rails
    - Sidekiq, AWS Batchを使った非同期,バッチ処理
    - Google Calendar連携
    - 決済を非同期にする
    - 検索時の合計料金
  - フロントエンド
    - Haml, Sass
    - React, Redux, Immutable.js等でのSPA、コンポーネント開発
      - 検索ページ
        - https://www.instabase.jp/search
      - スペース登録、編集フォーム
      - トップページ
       - https://www.instabase.jp
    - フロントエンドのパフォーマンスチューニング
      - オフスクリーンイメージの遅延読み込み
      - jsの分割
      - Reactコンポーネントのパフォーマンスチューニング
    - webpackのアップデート(1.x -> 4.x)
  - CI, CD
    - Circle CI
    - eslint, stylelintでリント
    - Rspec, capybara等でテスト

#### 検索APIサーバーの開発
- 主に[検索ページ](https://www.instabase.jp/search)で使われるAPIサーバーの開発
  - Scala, Finagle, Finch
  - 管理画面はTwitterServer
  - JSONを返す
  - Web(XHR)、Rubyからアクセス
  - DB
    - PostgreSQL(RDS)
    - Elastic Search(以下、ES)
      - ES内ドキュメントの検索、更新、追加、削除
  - API
    - 日時による検索
    - 緯度・経度による検索
    - フリーワードによる検索
    - 都道府県、設備等の条件による検索

### 2014/08 - 2015/12: 株式会社アカツキ
職務: サーバーサイドエンジニア
環境: Ruby(2.x), Ruby on Rails(4.x), MySQL(RDS), Redis(ElastiCache), CloudFront, EC2等

#### ゲームAPIサーバーの開発
- スマートフォンゲームのAPI開発
- ガチャ、ログインボーナス、インゲーム開始/終了、キャラクター合成/進化等
