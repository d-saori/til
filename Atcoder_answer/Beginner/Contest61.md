- A問題（https://atcoder.jp/contests/abc061/tasks/abc061_a）
```
a, b, c = gets.split.map(&:to_i)
# if a <= c <= b
#   puts "Yes"
# else
#   puts "No"
# end
# 三項演算子
puts a <= c && c <= b ? "Yes" : "No"
```

- B問題（https://atcoder.jp/contests/abc061/tasks/abc061_b）
```
n, m = gets.split.map(&:to_i)
ab = m.times.map { gets.split.map(&:to_i) }.flatten
(1..n).each { |i| puts ab.count(i) }
```
