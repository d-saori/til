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
<br>

# var、let、constの書き方
- 各キーワードの後に、変数名と、初期値を記述する。varとletは初期値を省略可能。
```
var hoge1 = 'hoge1';
var hoge2;  // 初期値を省略した書き方

let fuga1 = 'fuga1';
let fuga2;  // 初期値を省略した書き方

const piyo = 'piyo'; // constは初期値を省略できない。
```

# var、let、constのスコープ
- varとlet,constのスコープは異なる。
  - varはif文の外で宣言された場合、if文の中でも利用できる。<br>
  - letとconstはスコープ外となり利用できない。<br>
```
if (1) {
var x = 'OK';
let y = 'NG';
const z = 'NG';
}
console.log(x); //使用可能
console.log(y); //スコープ外のためエラー
console.log(z); //スコープ外のためエラー
```
