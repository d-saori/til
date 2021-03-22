- A問題（https://atcoder.jp/contests/abc145/tasks/abc145_a）

```
r = gets.to_i
puts r ** 2

# 1行で
puts gets.to_i ** 2
```

- B問題
```
n = gets.to_i
s = gets.chomp
c = n / 2
s_f = s[0..c-1]
s_e = s[c..-1]
puts n.even? && s_f == s_e ? "Yes" : "No"

# 別解
n = gets.to_i
s = gets.chomp
t = s[0, n / 2] * 2
puts s == t ? "Yes" : "No"
```

- C問題
```
n = gets.to_i
xy = n.times.map { gets.split.map(&:to_i) }
z = xy.combination(2).map { |a, b|
  Math.hypot(a[0] - b[0], a[1] - b[1])
}
puts z.sum / z.size * (n - 1)

# 別解
n = gets.to_i
x, y = n.times.map { gets.split.map(&:to_i) }.transpose
t = 0
(0..n-1).to_a.combination(2) { |a, b|
  t += Math.sqrt((x[a] - x[b]) ** 2 + (y[a] - y[b]) ** 2)
}
puts t * 2 / n
```
