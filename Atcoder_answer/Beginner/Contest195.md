- A問題
```
m, h = gets.split.map(&:to_i)
puts h % m == 0 ? "Yes" : "No"
```

- B問題
```
a, b, w = gets.split.map(&:to_f)
w = w * 1000
max = (w / a).floor
min = (w / b).ceil
puts max >= min ? [min, max].join(" ") : "UNSATISFIABLE"
```
