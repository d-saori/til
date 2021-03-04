- A問題
```
s, t = gets.split.map(&:to_i)
puts (s..t).size
```

- B問題
```
n = gets.to_i
s = n.times.map { gets.chomp }
puts s.max_by { |i| s.count(i) }
```
