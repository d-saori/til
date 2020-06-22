# form_withヘルパー
- Rails5.1で導入されたform_forヘルパーとform_tagヘルパー(https://qiita.com/Hal_mai/items/1e5afd0c99dd9059839f) の代わりとなるヘルパー<br>
- Viewファイルで使用することで、簡単にフォームを生成することができる<br>
- 入力値の送信先もシンプルに設定でき、コントローラへのデータ引き継ぎもスムーズに行うことができる<br>
```
<%= form_with model: モデルオブジェクト, local: true do |form| %>
・・・
<% end %>
```
- 「:local」オプション:(デフォルトでAjaxを使うようになっている)submitによるデータ送信にAjaxを使わないことを示すオプション<br>
  - 「local: true」:HTMLとしてフォームを送信する場合
- 「:model」オプション:生成するフォームがどのモデルに基づいて(このモデルから推測された送信先へ送信するフォームが生成)作られるかを示すオプション<br>
