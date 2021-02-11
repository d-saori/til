- A問題（https://atcoder.jp/contests/abc137/tasks/abc137_a）
```
a, b = gets.split.map(&:to_i)
puts [a + b, a - b, a * b].max
```

- B問題
```
k, x = gets.split.map(&:to_i)
min = x - k + 1
max = x + k - 1
puts (min..max).to_a.join(" ")
```
