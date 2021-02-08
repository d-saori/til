- A問題（https://atcoder.jp/contests/abc151/tasks/abc151_a）

```
c = gets
puts c.succ

# 1行でも可
puts gets.succ

# nextメソッドもある
```

- B問題
```
n, k, m = gets.split.map(&:to_i)
a = gets.split.map(&:to_i)
if a.sum / n >= m
  puts 0
elsif a.sum / n <= m && m * n - a.sum <= k
  puts m * n - a.sum
else
  puts -1
end

# 別解
n, k, m = gets.split.map(&:to_i)
a = gets.split.map(&:to_i).sum
if a + k < n * m
  puts -1
else
  puts [n * m - a, 0].max
end
```
