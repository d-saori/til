# 結論
- ルーティングが衝突してしまい、deviseのログイン画面が動かなくなったために起きた

```
resources :books
devise_for :users
```

<br>
とusersの上にbooksが書かれていたので以下のように修正
<br>

```
devise_for :users
resources :books
```
