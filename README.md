# README

## 環境構築
```
$ bundle install --without=production
$ bin/rails db:setup
$ yarn install
$ bin/webpack
$ bin/rails s
```

## 事業をエンジニアリングしよう提案編の回答は以下に記述してください

# 選択した事業側の課題

サービス登録者数の内、男性60%に対して、女性は40%。  
一方で、サービス内のもくもく会に参加した人の比率は、男性90%：女性10%と大きな差が出ています。  
もっと女性が使いやすいようなサービス設計にする必要があるのではないか？  
***

# 提案内容
ユーザー情報に性別と自己紹介を追加 + 他ユーザーの詳細(アイコン、名前、性別、自己紹介)が見れるようにする。  

-> 現状、主催者や参加者のプロフィールは見れないためどんな人が参加するのかわからない。   
そのため、登録したものの、参加に不安があるのではないかと思いました。  
また、元々エンジニアという職種的に男性が多いため、  
自分の他に女性参加者がいるのか？と不安になる方もいるかと思ったので  
性別欄の追加も実装したほうが参加率が上がるのではないかと思いました。  
***

# 実装方針
- ユーザー登録時に名前欄の下に、性別欄を追加する。  
- プロフィール編集ページで自己紹介(160文字)が入力できるようにする。(性別は編集の必要が無いので、編集欄は入れない) 
- ユーザー詳細ページを追加する。  
  - アイコン  
  - 名前  
  - 性別  
  - 自己紹介  
- もくもく会の詳細ページの主催者情報を押すと、主催者のユーザー詳細ページに飛ぶ。  
- もくもく会の詳細ページの参加者欄にいる、参加者の名前を押すとその人のユーザー詳細ページに飛ぶ。  

