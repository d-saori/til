- A問題（https://atcoder.jp/contests/abc129/tasks/abc129_a）

```
p, q, r = gets.chomp.split.map(&:to_i)
puts [p + q, r + q, r + p].min
```

- B問題
```
n = gets.to_i
w = gets.split.map(&:to_i)
ans = 0
sum = w.sum
puts w[0..-2].map { |i|
  ans += i
  sum -= i
  (ans - sum).abs
}.min

# 別解
n = gets.to_i
w = gets.split.map(&:to_i)
x = w.sum
y = 0
ans = n
n.times { |i|
  y += w[i]
  min = (x - y * 2).abs
  ans = min if ans > min
}
puts ans

# 別解
n = gets.to_i
w = gets.split.map(&:to_i)
sum = 0
ary = []
w.each { |i|
  sum += i
  ary << sum
}
puts ary.map { |j| (sum - 2 * j).abs }.min
```

- C問題
```
MOD = 1_000_000_007
n, m = gets.split.map(&:to_i)
dp = Array.new(m + 2)
m.times {
  a = gets.to_i
  dp[a] = 0
}
dp[n + 1] = 0
dp[n] = 1
p dp
(n - 1).downto(0) { |i|
  next if dp[i]
  dp[i] = (dp[i + 1] + dp[i + 2]) % MOD
}
puts dp[0]
```
