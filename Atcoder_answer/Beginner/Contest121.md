- A問題（https://atcoder.jp/contests/abc121/tasks/abc121_a）

```
h, w = gets.split.map(&:to_i)
a, b = gets.split.map(&:to_i)

puts (h - a) * (w - b)
```

- B問題
```
n, m, c = gets.split.map(&:to_i)
b = gets.split.map(&:to_i)
cnt = 0
n.times {
  a = gets.split.map(&:to_i)
  cnt += 1 if a.zip(b).map { |i, j| i * j}.sum + c > 0
}
puts cnt

# 別解
n, m, c = gets.split.map(&:to_i)
b = gets.split.map(&:to_i)
t = []
cnt = 0
n.times {
  a = gets.split.map(&:to_i)
  t << b.zip(a).map { |x, y|
    x * y
  }
}
puts t.select { |i|
  i.sum + c > 0
}.count
```

- C問題
```
n, m = gets.split.map(&:to_i)
ab = n.times.map { gets.split.map(&:to_i) }.sort
# ab = n.times.map { gets.split.map(&:to_i) }.sort_by { |a| a[0] }
sum = 0
ab.each { |x, y|
  break if m < 0
  sum += x * [m, y].min
  m -= y
}
puts sum
```
