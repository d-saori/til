- A問題（https://atcoder.jp/contests/abc108/tasks/abc108_a）

```
k = gets.to_i
# 偶数:k / 2
# 奇数:k - k / 2
# kまでの偶数と奇数を掛けた分通りの個数
puts (k / 2) * (k - k / 2)
```

- B問題
```
x1, y1, x2, y2 = gets.split.map(&:to_i)
x = x2 - x1
y = y2 - y1
puts [x2 - y, y2 + x, x1 - y, y1 + x].join(" ")
```
