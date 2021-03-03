- A問題
```
n = gets.to_i
puts n
n.times {
  puts 1
}
```

- B問題
```
n = gets.to_i
a, b = gets.split.map(&:to_i)
k = gets.to_i
p = gets.split.map(&:to_i)
route = [a, p, b].flatten
puts route.size == route.uniq.size ? "YES" : "NO"
```
