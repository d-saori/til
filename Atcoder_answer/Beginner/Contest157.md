- A問題（https://atcoder.jp/contests/abc157/tasks/abc157_a）

```
n = gets.chomp.to_i
puts (n / 2.to_f).ceil

もしくは
n = gets.to_f
puts (n / 2).round
```

- B問題
```
a = 3.times.map { gets.split.map(&:to_i) }.flatten
n = gets.to_i
v = []
n.times {
  x = gets.to_i
  idx = a.find_index(x)
  v[idx] = true if idx
}
puts [[0, 1, 2], [3, 4, 5], [6, 7, 8], [0, 3, 6], [1, 4, 7], [2, 5, 8], [0, 4, 8], [2, 4, 6]].any? { |i| i.all? { |j| v[j] }} ? "Yes" : "No"
```
