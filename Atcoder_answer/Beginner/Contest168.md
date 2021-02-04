- A問題(https://atcoder.jp/contests/abc168/tasks/abc168_a)

```
n = gets.chomp
if n[-1] == "3"
  puts "bon"
elsif n[-1] == "0" || n[-1] == "1" || n[-1] == "6" || n[-1] == "8"
  puts "pon"
else
  puts "hon"
end

もしくは
n = gets.chomp
if ["2", "4", "5", "7", "9"].include? n[-1]
  puts "hon"
elsif ["0", "1", "6", "8"].include? n[-1]
  puts "pon"
else
  puts "bon"
end
```

- B問題
```
k = gets.to_i
s = gets.chomp
puts s.size <= k ? s : "#{s[0..k-1]}..."
```
