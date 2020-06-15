- JavaScriptでは、変数や定数（以下、まとめて「変数」と表記）を使う際、変数名を宣言することが推奨されている。<br>
var、let、constとは、JavaScriptで変数を宣言する際に使うキーワード。<br><br>

# var
- 再宣言、再代入が可能<br>
```
var hoge = '初期値OK';
hoge = '再代入OK';
var hoge = '再宣言OK';
```

# let
- 再宣言が禁止されている<br>
```
var hoge = '初期値OK';
hoge = '再代入OK';
var hoge = '再宣言NG';
```

# const
- 再宣言、再代入が禁止されている<br>
```
var hoge = '初期値OK';
hoge = '再代入NG';
var hoge = '再宣言OK';
```


