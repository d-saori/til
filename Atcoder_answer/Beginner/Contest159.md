- A問題（https://atcoder.jp/contests/abc159/tasks/abc159_a）

```
# 偶数になる条件：偶数+偶数 or 奇数+奇数。奇数になる条件：偶数+奇数 なので『同じグループから2個選ぶ方法の数を求めれば良い』
# N個の中から選ぶ：N * (N - 1) / 2
# M個の中から選ぶ：M * (M - 1) / 2

n, m = gets.split.map(&:to_i) 
puts n * (n - 1) / 2 + m * (m - 1) / 2

# 別解答
n, m = gets.split.map(&:to_i) 
even = n.times.to_a
odd = m.times.to_a
puts even.combination(2).size + odd.combination(2).size
```
