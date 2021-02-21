- A問題
```
a, b = gets.split.map(&:to_i)
# (x + y) + (x - y) = 2x => x = (a + b) / 2
# (x + y) - (x - y) = 2y => y = (a - b) / 2
puts [(a + b) / 2, (a - b) / 2].join(" ")
```
