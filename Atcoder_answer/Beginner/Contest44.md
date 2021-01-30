- A問題（https://atcoder.jp/contests/abc044/tasks/abc044_a）
```
# n = gets.to_i
# k = gets.to_i
# x = gets.to_i
# y = gets.to_i
n, k, x, y = 4.times.map{gets.to_i}
puts n > k ? (k * x) + (n - k) * y : n * x
```

- B問題
```
w = gets.chomp.chars
cnt = w.group_by(&:itself).values.map(&:size)
puts cnt.all? { |i| i % 2 == 0 } ? "Yes" : "No"
```
