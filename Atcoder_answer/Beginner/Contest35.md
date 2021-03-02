- A問題
```
w, h = gets.split.map(&:to_i)
puts 3 * w == 4 * h ? "4:3 ": "16:9"

# 別解
w, h = gets.split.map(&:to_i)
puts w % 16 == 0 && h % 9 == 0 ? "4:3" : "16:9"
```
