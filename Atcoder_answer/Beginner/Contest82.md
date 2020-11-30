- A問題（https://atcoder.jp/contests/abc082/tasks/abc082_a）
```
a, b = gets.split.map(&:to_f)
puts ((a + b) / 2).ceil
```

- B問題（https://atcoder.jp/contests/abc082/tasks/abc082_b）
```
s = gets.chomp
t = gets.chomp
s1 = s.chars.sort.join
t1 = t.chars.sort.reverse.join
if s1 < t1
  puts "Yes"
else
  puts "No"
end

↓リファクタリング

s = gets.chomp.chars.sort.join
t = gets.chomp.chars.sort.reverse.join
 
puts s < t ? "Yes" : "No"
```
