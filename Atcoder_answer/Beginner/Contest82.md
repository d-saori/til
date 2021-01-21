- A問題（https://atcoder.jp/contests/abc082/tasks/abc082_a）
```
a, b = gets.split.map(&:to_f)
puts ((a + b) / 2).ceil
```

- B問題（https://atcoder.jp/contests/abc082/tasks/abc082_b）
```
s, t = 2.times.map { gets.chomp }
sa = s.chars.sort.join
ta = t.chars.sort.reverse.join
puts sa < ta ? "Yes" : "No"

# さらに省略
s = gets.chomp.chars.sort.join
t = gets.chomp.chars.sort.reverse.join
puts s < t ? "Yes" : "No"
```
