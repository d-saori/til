- A問題
```
l = gets.split.map(&:to_i)
puts l[0] == l[1] && l[0] == l[2] ? l[0] : l.select { |i| l.count(i) <= 1}

# 別解
l = gets.split.map(&:to_i)
puts l.find { |i| l.count(i) % 2 == 1 }
```

- B問題
```
n = gets.to_i
a = gets.split.map(&:to_i)
b = a.sum
if b % n == 0
  m = b / n
  puts (0..n-1).count { |i|
    a[0...i].sum != i * m
  }
else
  puts -1
end
```
