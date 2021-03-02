- A問題
```
a, b, c = gets.split.map(&:to_i)
# min = [a, b].min
puts c / [a, b].min
```

- B問題
```
n, q = gets.split.map(&:to_i)
f = Array.new(n, 0)
q.times {
  l, r, t = gets.split.map(&:to_i)
  f.fill(t, l-1..r-1)
}
puts f
```
