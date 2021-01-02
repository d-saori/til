- A問題（https://atcoder.jp/contests/abc187/tasks/abc187_a）
```
a, b = gets.split
a_sum = a.chars.map(&:to_i).sum
b_sum = b.chars.map(&:to_i).sum
puts [a_sum, b_sum].max
```
