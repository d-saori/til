- A問題（https://atcoder.jp/contests/abc159/tasks/abc159_a）

```
# 偶数になる条件：偶数+偶数 or 奇数+奇数。奇数になる条件：偶数+奇数 なので『同じグループから2個選ぶ方法の数を求めれば良い』
# N個の中から選ぶ：N * (N - 1) / 2
# M個の中から選ぶ：M * (M - 1) / 2

n, m = gets.split.map(&:to_i) 
puts n * (n - 1) / 2 + m * (m - 1) / 2

# 別解
n, m = gets.split.map(&:to_i) 
even = n.times.to_a
odd = m.times.to_a
puts even.combination(2).size + odd.combination(2).size

# 別解
n, m = gets.split.map(&:to_i)
even = [*0..n-1].combination(2).to_a
odd = [*0..m-1].combination(2).to_a
puts even.size + odd.size
```

- B問題
```
# 回文(前から読んでも後ろから読んでも同じ)なので文字列は奇数長
# 文字列を中央で分けた時、前と後ろそれぞれの文字列も回文
s = gets.chomp
n = s.size / 2
puts s == s.reverse && s[0, n] == s[0, n].reverse ? "Yes" : "No"
```

- C問題
```
l = gets.to_f
puts (l / 3.0) ** 3
```
