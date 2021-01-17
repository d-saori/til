- A問題
```
a = gets.to_i
b = gets.to_i
c = gets.to_i
d = gets.to_i
ab = [a, b].min
cd = [c, d].min
puts ab + cd

# 短く
a, b, c, d = 4.times.map {gets.to_i}
puts [a, b].min + [c, d].min
```
