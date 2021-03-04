- A問題
```
m, d = gets.split.map(&:to_i)
puts m % d == 0 ? "YES" : "NO"
```

- B問題
```
a, b, c = gets.split.map(&:to_i)
p = a + b
m = a - b
if p == c && m == c
  puts "?"
elsif m == c
  puts "-"
elsif p == c 
  puts "+"
else
  puts "!"
end
```
