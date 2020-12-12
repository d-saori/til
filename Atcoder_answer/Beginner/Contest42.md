- A問題（https://atcoder.jp/contests/abc042/tasks/abc042_a）
```
a, b, c = gets.chomp.split.map(&:to_i)
if [a, b, c] == [5, 5, 7] || [a, b, c] == [5, 7, 5] || [a, b, c] == [7, 5, 5]
  puts "YES"
else
  puts "NO"
end

もしくは
a, b, c = gets.chomp.split.map(&:to_i)
if [a, b, c].sort == [5, 5, 7]
  puts "YES"
else
  puts "NO"
end
```

- B問題（https://atcoder.jp/contests/abc042/tasks/abc042_b）
```
n, l = gets.split.map(&:to_i)
s = n.times.map{gets.chomp.to_s}.sort
puts s.join
```
