- A問題（https://atcoder.jp/contests/abc130/tasks/abc130_a）

```
x, a = gets.split.map(&:to_i)
puts x < a ? 0 : 10
```

- B問題
```
n, x = gets.split.map(&:to_i)
l = gets.split.map(&:to_i)
cnt = 1
sum = 0
(0..n-1).each { |i|
  sum = sum + l[i]
  cnt += 1 if sum <= x
}
puts cnt

# 別解
n, x = gets.split.map(&:to_i)
l = gets.split.map(&:to_i)
cnt = 1
sum = 0
l.each { |i|
  sum += i
  cnt += 1 if sum <= x
}
puts cnt

# 別解
n, x = n, x = gets.split.map(&:to_i)
l = gets.split.map(&:to_i)
sum = 0
puts l.map { |i| sum += i }.count { |j| j <= x } + 1
```
