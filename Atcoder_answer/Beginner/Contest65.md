- A問題
```
x, a, b = gets.split.map(&:to_i)
if b - a <= 0
  puts "deliciou"
else
  puts x >= b - a ? "safe" : "dangerous"
end
```
