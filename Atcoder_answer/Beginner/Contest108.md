- A問題（https://atcoder.jp/contests/abc108/tasks/abc108_a）

```
k = gets.to_i
# 偶数:k / 2
# 奇数:k - k / 2
# kまでの偶数と奇数を掛けた分通りの個数
puts (k / 2) * (k - k / 2)
```