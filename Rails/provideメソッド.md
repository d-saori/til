# provideメソッド
- 日本語に訳すと「供給する」「与える」

```
# provideメソッドを使って、`マイページ`という個別のタイトルを設定。レイアウトファイルでは設定されたタイトルをyieldで表示。
<% provide :title, "マイページ" %>
```

- application.html.erb(レイアウトファイル:各viewで共通している部分のHTMLを書くファイル)

```
<title><%= yield(:title) %> | Ruby on Rails Tutorial Sample App</title>
```
