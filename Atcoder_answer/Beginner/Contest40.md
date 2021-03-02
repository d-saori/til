- A問題
```
n, x = gets.split.map(&:to_i)
puts [x - 1, n - x].min
```

- B問題
```
n = gets.to_i
ans = n
d = 1
while d * d <= n
  h, w = n.divmod(d) # => h:商 w:余り
  ans = [ans, h - d + w].min
  d += 1
end
puts ans
```
