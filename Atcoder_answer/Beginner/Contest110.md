- A問題（https://atcoder.jp/contests/abc110/tasks/abc110_a）

```
a = gets.split.map(&:to_i)
# 3つの数字を昇順に並べる
a.sort!
# 1番大きい3つ目の要素(インデックス番号2)が10の桁 = *10
puts a[2] * 10 + a[1] + a[0]
```
