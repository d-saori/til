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
