- A問題
```
a = gets.chomp
ary = ["A", "B", "C", "D", "E"]
puts ary.index(a) + 1
```

- B問題
```
a, b = 2.times.map { gets.to_i }
n = (a - b).abs
puts n < 5 ? n : 10 - n
```
