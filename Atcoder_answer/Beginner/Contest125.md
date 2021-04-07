- A問題（https://atcoder.jp/contests/abc125/tasks/abc125_a）

```
a, b, t = gets.split.map(&:to_i)
c = (t + 0.5) / a
puts c.floor * b

# 別解
a, b, t = gets.split.map(&:to_i)
puts (t / a) * b
```

- B問題（https://atcoder.jp/contests/abc125/tasks/abc125_b）
```
n = gets.to_i
v = gets.split.map(&:to_i)
c = gets.split.map(&:to_i)
# i番目の宝石を選ぶ事によってX-YはVi-Ciだけ変化する。
# コストよりも価格が高いような宝石のみを手に入れるのが最適
t = []
(0..n-1).each { |i|
  s = v[i] - c[i]
  t << s if s > 0
}
puts t.size == 0 ? 0 : t.sum

# 別解
n = gets.to_i
v = gets.split.map(&:to_i)
c = gets.split.map(&:to_i)

# x - y > 0 = 宝石を選ぶ(加算される)
ans = 0
v.zip(c).map{ |x, y| ans += x - y if x > y}
puts ans
```

- C問題
```
n = gets.to_i
a = gets.split.map(&:to_i)
d = 0
s = a.map { |i|
  d = d.gcd(i)
}
d = 0
t = a.reverse.map { |i|
  d = d.gcd(i)
}.reverse
puts n.times.map { |i|
  (i > 0 ? s[i - 1] : 0).gcd(i < n - 1 ? t[i + 1] : 0)
}.max
```
