- A問題(https://atcoder.jp/contests/abc161/tasks/abc161_a)

```
x, y, z = gets.split.map(&:to_i)
puts "#{z} #{x} #{y}"

# 別解答例
x, y, z = gets.split(" ").map(&:to_i)
puts [z, x, y].join(" ")
```

- B問題
```
n, m = gets.split.map(&:to_i)
a = gets.split.map(&:to_i).sort.reverse
poll = a.sum
puts m <= a.count { |i| i >= poll / (4.0 * m) } ? "Yes" : "No"

# 別解
n, m = gets.split.map(&:to_i)
a = gets.split.map(&:to_i).sort.reverse
poll = a.sum / (4.0 * m)
puts a[m - 1] >= poll ? "Yes" : "No"
```
