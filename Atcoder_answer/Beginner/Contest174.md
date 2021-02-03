- A問題（https://atcoder.jp/contests/abc174/tasks/abc174_a）

```
x = gets.to_i
puts x >= 30 ? "Yes" : "No"
```

- B問題
```
n, d = gets.split.map(&:to_i)
m = []
n.times {
  x, y = gets.split.map(&:to_i)
  z = ((x ** 2) + (y ** 2)) ** 0.5
  m << z if z <= d 
}
puts m.size

# 別解
# dも2乗して平方根を取る
n, d = gets.split.map(&:to_i)
cnt = 0
n.times {
  x, y = gets.split.map(&:to_i)
  cnt += 1 if x * x + y * y <= d * d
}
puts cnt
```
