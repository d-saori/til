- A問題（https://atcoder.jp/contests/abc173/tasks/abc173_a）


```
n = gets.to_i
# 1000円札のみで支払いを行う以上、nの下3桁のみがお釣りの金額に関係する
puts (n - n % 1000) % 1000
```
