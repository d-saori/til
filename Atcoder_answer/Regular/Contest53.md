- A問題
```
h, w = gets.split.map(&:to_i)
t = []
s = []
(1..h).each_cons(2) { |i| t << i }
(1..w).each_cons(2) { |j| s << j }
puts t.size * w + s.size * h
```
