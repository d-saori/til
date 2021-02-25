- A問題
```
n = gets.chomp.chars
puts n.reverse == n ? "Yes" : "No"
```

- B問題
```
a, b, c, d = gets.split.map(&:to_i)
puts [[b, d].min - [a, c].max, 0].max
```
