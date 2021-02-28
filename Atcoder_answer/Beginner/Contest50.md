- A問題
```
a, op, b = gets.chomp.split
puts op == "+" ? a.to_i + b.to_i : a.to_i - b.to_i
```

- B問題
```
n = gets.to_i
t = gets.split.map(&:to_i)
all = t.sum
m = gets.to_i
m.times {
  p, x = gets.split.map(&:to_i)
  puts all - t[p - 1] + x
}
```
