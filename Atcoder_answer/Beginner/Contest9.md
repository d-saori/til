- A問題
```
n = gets.to_f
puts (n / 2).ceil
```

- B問題
```
n = gets.to_i
a = n.times.map { gets.to_i }.sort
a.delete(a[-1])
puts a[-1]
```
