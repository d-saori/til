- A問題
```
n = gets.to_i
if n <= 59
  puts "Bad"
elsif n >= 60 && n <= 89
  puts "Good"
elsif n >= 90 && n <= 99
  puts "Great"
else
  puts "Perfect"
end
```

- B問題
```
s = gets.chomp
ans = ("A".."F").map { |i| s.count(i) }
puts ans.join(" ")
```
