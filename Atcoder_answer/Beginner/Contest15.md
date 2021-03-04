- A問題
```
a, b = 2.times.map { gets.chomp }
puts a.size > b.size ? a : b
```

- B問題
```
n = gets.to_i
a = gets.split.map(&:to_i)
b = a.select { |i| i > 0 }.count
puts (a.sum / b.to_f).ceil
```
