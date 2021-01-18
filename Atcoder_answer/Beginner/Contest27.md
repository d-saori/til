- A問題
```
l = gets.split.map(&:to_i)
puts l[0] == l[1] && l[0] == l[2] ? l[0] : l.select { |i| l.count(i) <= 1}

# 別解
l = gets.split.map(&:to_i)
puts l.find { |i| l.count(i) % 2 == 1 }
```
