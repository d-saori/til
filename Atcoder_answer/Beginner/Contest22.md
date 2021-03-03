- A問題
```
n, s, t = gets.split.map(&:to_i)
cnt = 0
w = 0
n.times {
  w += gets.to_i
  cnt += 1 if s <= w && w <= t
}
puts cnt

# 別解
n, s, t = gets.split.map(&:to_i)
w = gets.to_i
cnt = 0
n.times {
  a = gets.to_i
  cnt += 1 if s <= w && w <= t
  w += a
}
puts cnt
```

- B問題
```
n = gets.to_i
a = n.times.map { gets.to_i }
puts n - a.uniq.count
```
