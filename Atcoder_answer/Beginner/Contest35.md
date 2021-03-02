- A問題
```
w, h = gets.split.map(&:to_i)
puts 3 * w == 4 * h ? "4:3 ": "16:9"

# 別解
w, h = gets.split.map(&:to_i)
puts w % 16 == 0 && h % 9 == 0 ? "4:3" : "16:9"
```

- B問題
```
s = gets.chomp
t = gets.to_i
x, y = 0, 0
x -= s.count("L")
x += s.count("R")
y -= s.count("U")
y += s.count("D")
z = s.count("?")
d = x.abs + y.abs
puts t == 1 ? d + z : [d - z, s.size % 2].max
```
