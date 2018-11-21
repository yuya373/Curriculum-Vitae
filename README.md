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
  - Ruby on Rails (v3 ~ v4)
- JavaScript
  - webpack (v1 ~ v4)
  - babel (v??? ~ v6)
  - React (v??? ~ v16)
  - react-router (v3 ~ v4)
  - Redux
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
  - 公式チュートリアル + α
    - [yuya373/FoodTracker](https://github.com/yuya373/FoodTracker)
  - Dropboxに保存するメモ帳
    - [yuya373/Note](https://github.com/yuya373/Note)
- Rust
  - 本やチュートリアルの写経
    - [yuya373/programming-rust](https://github.com/yuya373/programming-rust)
    - [yuya373/trpl](https://github.com/yuya373/trpl)
    - [yuya373/line-chat](https://github.com/yuya373/line-chat)
    - [yuya373/rust_dns](https://github.com/yuya373/rust_dns)
- Unity, C#
  - チュートリアル
    - [yuya373/Roll-a-Ball](https://github.com/yuya373/Roll-a-Ball)
  - Oculus Go用のシューティングアプリ
    - [yuya373/VRShootingGame](https://github.com/yuya373/VRShootingGame)

## やったことはないが興味があるもの
- iOSアプリ開発
- ミドルウェア開発

## 職務経歴

### 2016/01 - : 株式会社Rebase
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
