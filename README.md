# 『ねこねこFinder』

## サービス概要
- 迷子の猫を見つけるための情報共有プラットフォーム
- ユーザーが猫の情報を登録し、カスタマイズ可能な迷子チラシを作成
- SNS共有機能を通じて迷子猫の情報を広く拡散

## このサービスへの思い・作りたい理由
- 電柱や動物病院に貼られることが多い迷子猫のチラシを見て、自身も猫を飼っている身として飼い主と猫の心境を想像すると心苦しく、手助けできるようなアプリを作りたいと受講前から考えていた
- テンプレート使用で、Web上で簡単に作成できるチラシを用いて、SNSでの拡散と印刷して地域に配布することでチラシとSNSの利点を組み合わせ、飼い主と迷子猫の再会効果を高めたい

## ユーザー層について
- 迷子猫の飼い主：
  - 迷子の猫を効果的に探すためのサポートが必要なため
- 金銭的余裕がない飼い主
  - 金銭的余裕がなく、猫を探す依頼などが出せなくても利用してほしい
- 猫の保護活動をする団体・個人：
  - 迷子の猫の情報を共有し、再会を助けるため

## サービスの利用イメージ
- ユーザーは迷子の猫の情報を入力し、カスタマイズ可能な迷子猫チラシを作成できる
- 作成したチラシはSNSで共有し、印刷して電柱に貼る、配布する（動物病院や街頭など）ことも可能
- 迷子の猫の情報が広く拡散され、再会の可能性が高まる

## ユーザーの獲得について
- 猫のコミュニティ、フォーラム、SNSでサービスを紹介
  - アプリ専用のSNSアカウントを作り、地道なサービスの普及活動を行う（MVP後）
- 猫の保護活動をする団体や動物病院などにも連携で情報を広める
  - まずは、かかりつけの動物病院で話を聞いてもらえるか感触を確かめる
  - SNSアカウントを通じて、保護猫活動をしている個人や団体にPR
## サービスの差別化ポイント・推しポイント
- デザインができなくてもテンプレートに入力することで迷子チラシを簡単に作成
- SNS共有機能を通じてオンラインとオフラインで情報を広める（デジタルとアナログの両方で効率的な迷子猫探しをサポート）
- 無料

## 機能候補
### MVPリリース時に作っていたい機能
- ユーザー登録
- ログイン機能
  - Xアカウントでもログイン可能
- プロフィール編集機能
- 迷子チラシのテンプレート機能
  - 複数のデザインテンプレートを用意し、ユーザーは好みのテンプレートを選択できる
  - テンプレートには、猫の名前、年齢、性別、特徴（色、模様、体型など）、最後に目撃された場所と時間、連絡先や詳細（追加で記載したいことがある倍に使用を想定）などの入力欄に入力できる
  - ユーザーは画像アップロード機能を使用して、猫の画像をチラシに挿入することができる
- 画像アップロード機能
- プレビュー機能
- 迷子猫情報の作成・編集・削除機能
- コメント機能
- SNS共有機能
### 本リリースまでに作っていたい機能
- 地域別の迷子猫情報データベース
  - 迷子猫情報を保存するためのデータベースを作る。猫の名前、特徴、最後に目撃された日時、場所（緯度経度情報を含む）などの情報を含める
- ユーザーからの目撃情報
  - ユーザーから提供された目撃情報をフォーム入力してもらうことでデータベースに保存
- 検索機能
- LINE通知

## 機能の実装方針予定
 迷子チラシのテンプレート機能：
  - 複数のテンプレートを提供し、ユーザーが必要な情報を入力してカスタマイズ可能
  - @vercel/ogなどを用いた動的な画像生成を検討

- 画像アップロード機能：
  - ActiveStorageやCarrierWaveを使用してユーザーが画像をアップロードできるようにする
  - ImageMagickやMiniMagickを使用して画像のサイズ調整や最適化を行う
  - CloudinaryやAmazon S3などのクラウドストレージサービスを利用して画像を安全に保存

- 位置情報（迷子猫情報データベース）：
  - Google Maps Platformを使用して、迷子猫の目撃情報を地図上に表示

- 検索機能：
  - マルチカラム検索とオートコンプリート機能を実装して、ユーザーが簡単に情報を検索できるようにする

- LINE通知：
  - ユーザーからの目撃情報が寄せられると、関連するユーザーに通知が飛ぶ機能を実装

## 画面遷移図
https://www.figma.com/file/jLXn6Ymt79a5OcaTQcM3ow/nekoneko_finder?type=design&node-id=0%3A1&mode=design&t=5v1U84SYQPFG4Her-1

## ER図
https://gyazo.com/3029462779375a3f363b8ef5097060a6
