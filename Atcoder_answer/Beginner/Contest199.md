- A問題
```
a, b, c = gets.split.map(&:to_i)
puts a ** 2 + b ** 2 < c ** 2 ? "Yes" : "No"
```

- B問題
```
# 条件(1 ≤ Ai ≤ Bi ≤ 1000)よりA.max ≤ x ≤ B.min
# [0, B.min - A.max + 1].max
n = gets.to_i
a = gets.split.map(&:to_i)
b = gets.split.map(&:to_i)
puts [0, b.min - a.max + 1].max


```
