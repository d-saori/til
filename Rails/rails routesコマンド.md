# rails routesコマンド
- routes.rbで記述したルーティングをターミナルで確認することができるコマンド<br>
- 「Prefix」 「Verb」 「URI Pattern」 「Controller#Action」 という4つの出力結果の項目がある<br><br>

# Prefix
パスが入った変数のようなもの。Prefixをパスとして使いたい場合は、末尾に「_path」を追記する。<br><br>

```
<%= link_to "詳細", tweets_path('tweetのidが入ったインスタンス') %>

# Prefixの箇所をURI（URL）で指定した場合
<%= link_to '詳細', "/tweets/#{tweet.id}" %>
```

# Verb
HTTPメソッドを表す。URI Patternのパスにどのhttpリクエストでアクセスするかを示している。<br><br>

- GET:リソースの取得。単にウェブサイトを閲覧する際に使用。<br>
- POST:リソースの保存。情報を登録する際に、サーバーに情報を送信するために使用。<br>
- DELETE:リソースの削除。アカウント削除の際に、サーバー内のデータを削除するために使用。<br>
- PATCH:リソースの更新。登録情報の更新の際に、サーバー内のデータを更新するために使用。<br><br>

# URI Pattern
ルーティングのパスを表す。このパスにアクセスされた際に、指定のコントローラとアクションで処理が行われる。<br><br>

# Controller#Action
httpリクエストでパスが送られた際に、処理が行われるコントローラとアクションを表す。<br>
  - 例）tweets#indexと書かれていれば、tweetsコントローラーのindexアクションという意味<br><br>
  

