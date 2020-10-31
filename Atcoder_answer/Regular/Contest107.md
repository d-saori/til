- A問題（https://atcoder.jp/contests/arc107/tasks/arc107_a）
  - 解説(https://atcoder.jp/contests/arc107/editorial/260)

```
a, b, c = gets.split.map(&:to_i)
r = 998244353
ans = a * (a + 1) * b * (b + 1) * c * (c + 1) / 8
puts ans % r
```
