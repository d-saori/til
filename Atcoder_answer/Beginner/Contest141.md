- A問題（https://atcoder.jp/contests/abc141/tasks/abc141_a）

```
s = gets.chomp
if s == "Sunny"
  puts "Cloudy"
elsif s == "Cloudy"
  puts "Rainy"
else
  puts "Sunny"
end

もしくは

s = %w(Sunny Cloudy Rainy)
puts s[s.index(gets.chomp) - 2]
```

- B問題
```
s = gets.chomp.chars
odd = s.select.with_index { |_, i| i.even? }
even = s.select.with_index { |_, i| i.odd? }
puts odd.each.count { |i| "RUD".include?(i) } + even.each.count { |j| "LUD".include?(j) } == s.size ? "Yes" : "No"
```
