- A問題
```
n = gets.chomp.chars
puts n.reverse == n ? "Yes" : "No"
```

- B問題
```
a, b, c, d = gets.split.map(&:to_i)
puts [[b, d].min - [a, c].max, 0].max

# 別解
a, b, c, d = gets.split.map(&:to_i)
max = [a, c].max
min = [b, d].min
puts max < min ? min - max : 0
```

- C問題
```
n = gets.to_i
t = n.times.map { gets.to_i }
t.uniq!
puts t.inject { |a, b| a.lcm(b) }
```
