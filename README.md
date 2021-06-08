# 経歴（2021 年 6 月更新）

## 基本情報

| 項目 | 概要         
| ---- | ---
| 名前 　　| 比嘉　恵作（ひが　けいさく） 
| 生まれ   | 沖縄県読谷村 
| 誕生日   | 1988年06月19日
| 英語     | TOEIC=910(L=470,R=440), IELTS=6.5(R=7.0,L=6.0,W=6.0,S=6.0)   
| Twitter          | https://mobile.twitter.com/khiga619
| Qiita            | https://qiita.com/KeisakuHiga   
| LinkedIn         | https://www.linkedin.com/in/keisakuhiga/
| 趣味   | バスケ・ゴルフ・散歩・筋トレ・暗号資産・シストレ開発
| これまで住んだ場所   | 沖縄→大阪→東京→ジャカルタ→メルボルン→千葉（←今ここ）

## 技術経験

|              | プログラミング言語               | フレームワーク                       | DB         | OS             | ブロックチェーン関連 | ツール                                                                  |
| ------------ | -------------------------------- | ------------------------------------ | ---------- | -------------- | -------------------- | ----------------------------------------------------------------------- |
| 実務         | Typescript, Javascript, Solidity | Node.js, Express, Vue, Nuxt, Truffle | Postgresql | Windows, Linux | Ethereum, Geth       | Github, VS Code, Slack, Zoom, Asana, Confluence, Share Point(Office365) |
| プライベート | Ruby                             | Ruby on Rails, React                 | MongoDB    | MacOS          | Ganache, Infura      | Trello, Discord, Figma                                                  |

## 開発工程の経験

|              | 要件定義 | 基本設計 | 詳細設計 | プログラミング       | テスト | 保守・運用 | デザイン(UI・UX) | インフラ | マネジメント | 手法               |
| ------------ | -------- | -------- | -------- | -------------------- | ------ | ---------- | ---------------- | -------- | ------------ | ------------------ |
| 実務         | ×        | ▲ ※1     | ◯        | フロント ◯, バック ◯ | ▲ ※2   | ×          | ×                | ×        | ×            | ウォーターフォール |
| プライベート | ◯        | ◯        | ◯        | フロント ◯, バック ◯ | ◯      | ×          | ◯                | ×        | ◯            | ウォーターフォール |

※1: 基本設計資料（画面遷移図、ER 図、テーブル定義書、API 一覧、項目定義一覧、コード値一覧）の追記・修正。  
※2: 単体テスト・結合テストはブラックボックスで実施。テストケースを洗い出し、手動で実施。

## プロジェクト詳細

1. ### 水産物トレーサビリティーアプリケーション開発プロジェクト （2020 年 10 月〜現在）

   【プロジェクト概要】

   - 水産物のトレーサビリティによりサステナブルな漁業を実現させることを目的としたプロジェクト。
   - プログラミング言語はTypeScriptを採用し、フロントエンドに Vue.js、バックエンドに Node.js を活用し開発中。
   - 開発メンバー体制
      - 立ち上げフェーズ: 5名（2020年〜2021年02月＠ウォーターフォール開発）
      - 直近: 2〜４名（2021年03月〜現在＠スクラム開発）

   【プログラミング言語/フレームワーク/ライブラリ/DB など】  
   　 Typescript, Node.js, Express.js, Vue.js, Nuxt.js, Postgresql

   【担当分野・実装した機能・実装方法】
   - 詳細設計・開発・単体テスト・結合テスト・リリースなど開発業務全般
   - フロントエンド（Vue/Nuxt）
      - 画面定義書作成
      - 画面作成（動作ロジックのみ、HTML/CSSはデザイナー提供）
      - 画面テスト
   - バックエンド（Node）
      - API仕様書作成
      - API開発
      - API単体テスト

1. ### 某ブロックチェーンスタートアップの Dapps 受託開発（2019 年 12 月〜2020 年 4 月）

   【プロジェクト概要】

   - ブロックチェーン技術を利用した BtoC サービスの受託開発
   - ERC20 ベースで独自トークンを発行する機能があり、それを顧客自身の情報と交換する

   【プログラミング言語/フレームワーク/ライブラリ/DB など】  
   　 Javascript, Ethereum, Geth, Solidity, Truffle, Web3.js, Node.js, Express.js, Vue.js, Nuxt.js, Postgresql

   【担当分野・実装した機能・実装方法】

   1. Ethereum、Solidity、web3.js の技術検証、PoA（Clique）のファイナリティの調査。
   1. ブロックチェーン関連の API 呼び出しに関わるビジネスロジック、スマートコントラクトとのトランザクション関連のプログラム設計、実装、単体テストを担当。web3.js 使用。
      Metamask などのウォレット使用を前提としない仕様で、秘密鍵は AWS/KMS で暗号化された状態で DB に保管する仕様であった。トランザックション発効の際には復号化された秘密鍵で署名するように実装。
   1. Vue.js 使用したフロントエンド開発。管理者画面ページの API 埋め込みなどを一部実装。

   【発揮したバリュー】  
   スマートコントラクト、バックエンド、フロントエンドの３つの領域にまたがって幅広く開発工程に貢献した。この３領域のエンジニアメンバーと密にコミュニケーションしながら、ブロックチェーン関連機能の設計・実装・テストの工程を進められたのは大きなバリューになったと確信している。

   【直面した技術的課題とその解決手法】

   1. call メソッドはスマートコントラクト側で設定した例外メッセージを捕捉出来る一方、sendSignedTransaction メソッドは web3.js の仕様上不可能であった。保守運用フェーズにおけるスマートコントラクト関連のバグに対応する為の妥協案として、アプリケーションサーバーサイドでどのようなトランザクションを発行したかというログを残す仕様にして対応。
   1. スマートコントラクトへのトランザクション発行時に使用する web3.js の estmateGas メソッド関連でトランザクションが発行できないバグに行き詰まった。試行錯誤末、スマートコントラクトの ABI からそのトランザクションが実行可能かを事前判断する仕様に気づく事ができ同バグを解消した。スマートコントラクト

   【チーム構成】

   - リードエンジニア１名
   - インフラエンジニア２名
   - スマートコントラクトエンジニア１名
   - バックエンド＆フロントエンド４名（← 私はここ。）

1. ### DeFi/Compound を活用した Dapps プロトタイプ開発（2019 年 9 月〜2019 年 10 月：インターンシップ）

   【プロジェクト概要】  
   Compound と rTokenContract を活用した DApp プロトタイプ開発プロジェクト。Compound にて StableCoin の一つである DAI を運用し、その運用で得られた利子が設定金額に到達した段階で同 DApp ユーザーはある商品を獲得出来るというサービス。開発環境（Ethereum）はパブリックチェーンの testnet（Rinkeby）を使用。

   ソースコード（GitHub）は[こちら](https://github.com/KeisakuHiga/FlexDappHoodie)。尚、このプロジェクトは、私がオーストラリア・メルボルンにあるブロックチェーンスタートアップにインターンシップしている際に参画したもの。

   【プログラミング言語/フレームワーク/ライブラリ/DB など】  
   Ethereum, Solidity, Truffle, Javascript, web3.js, React, Infura

   【担当分野・実装した機能・実装方法】  
   スマートコントラクトの設計・実装・テストまでを担当。

   【発揮したバリュー】

   - はじめての Dapps 開発で、開発言語やフレームワークについても全くの未経験で、チームからのサポートもありながらではあったが、ほぼ独学で Dapps 開発手法を学習し 2 ヵ月でプロトタイプ完成まで至れた事。
   - プロジェクト参画直後、リードエンジニアからプロトタイプの概要を伝えられた後、細かな仕様を自ら検討し、スマートコントラクトを設計・実装・テストまでの工程に対応した事。

   【直面した技術的課題とその解決手法】

   - 私の課題  
     開発言語やフレームワーク、Compound や rTokenContract などの外部スマートコントラクトの活用など、Dapps 開発の基礎が全くのゼロからのスタートであったこと。

   - 対応策  
     まずはトークンを発行したり送付したりする簡単なスマートコントラクトを実装する事で基礎を固めた。そして、外部スマートコントラクトの仕様等については、公式ドキュメントや README などを注意深く読み込みながらプロトタイプ開発に反映させていくことを地道に行い、Dapps の開発手法を自分なりに確立した。

   【チーム構成】

   - リードエンジニア１名
   - スマートコントラクトエンジニア 1 名（← 私はここ。）
   - サポートエンジニア２名（← 開発には参画せず、私にサポートをくれました。）

1. ### スイーツ予約管理システム開発プロジェクト（2019 年 7 月：プログラミングスクール、グループ課題）

   【プロジェクト概要】  
   メルボルンにあるスイーツショップ向け商品予約管理システム開発プロジェクト。MERN スタック（MongoDB, Express.js, React, Node.js）学習課程の課題として、実際に顧客を探し、ヒアリングを行い、その顧客が抱える課題を Web アプリケーションで解決しようと取り組んだもの。ソースコード（GitHub）は[こちら](https://github.com/KeisakuHiga/cherrys-bake-shop)。

   【プログラミング言語/フレームワーク/ライブラリ/DB など】  
   HTML, CSS, Javascript, Node.js, Express.js, React, MongoDB

   【担当分野・実装した機能等\_使用技術】

   - 担当分野：企画、要件定義、設計、実装（主にバックエンド）
   - 実装した機能等：
     1. ZEIT/Now（サーバー）、MongoDB Atlas（DB）及び Netlify（フロント）の開発環境のセッティングと本番環境へのデプロイメント
     1. ログイン・ログアウト機能 - JWT
     1. サーバーサイドでの Validation 機能 - Joi
     1. データベース Entity Relationship Diagrams の作成
     1. アプリケーション全体の設計（Client-Server-Database）

   【発揮したバリュー】

   - 実装工程において全般的にチームメイトをリードしプロジェクト推進した点。
   - オーストラリア人のチームメイトと英語でプロジェクトに取り組んだ点。

   【チーム構成】

   - Web エンジニア 3 名（← 私はここ。）

1. ### CtoC レンディング Web サービス開発プロジェクト（2019 年 5 月：プログラミングスクール、グループ課題）

   【プロジェクト概要】  
   Ruby / Ruby on Rails の学習課程の課題として、ツー・サイド・プラットフォーム Web サービス開発があり、個人間の金銭貸借 Web サービスを企画・開発に取り組んだプロジェクト。ソースコード（GitHub）は[こちら](https://github.com/KeisakuHiga/rails-project)。

   【プログラミング言語/フレームワーク/ライブラリ/DB など】  
   HTML, CSS, Bootstrap, Ruby, Ruby on Rails, Postgresql, AWS/S3, Heroku, Stripe

   【担当分野・実装した機能等\_使用技術】

   - 担当分野：企画、要件定義、設計、実装（フロントエンド＆バックエンド）
   - 実装した機能：
     1. ログイン・ログアウト機能及びアクセス制限機能の実装 - Devise|CanCanCan
     1. 画像アップロード機能 - AWS S3
     1. オンライン決済機能 - Stripe
     1. データベース Entity Relationship Diagrams の作成

   【発揮したバリュー】

   - 企画から実装までの工程で全般的にチームメイトをリードしプロジェクト推進した点。
   - 金融知識を活かして金銭貸借期間中の金利計算ロジックの実装部分で大きく貢献した点。
   - オーストラリア人のチームメイトと英語でプロジェクトに取り組んだ点。

   【チーム構成】

   - Web エンジニア 2 名（← 私はここ。）
