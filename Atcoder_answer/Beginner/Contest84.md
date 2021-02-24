- A問題
```
m = gets.to_i
puts 24 - m + 24

# 別解
m = gets.to_i
puts 48 - m
```

- B問題
```
a, b = gets.split.map(&:to_i)
s = gets.chomp
puts s.match(/\d{#{a}}-\d{#{b}}/) ? "Yes" : "No"
```
