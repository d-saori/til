- A問題
```
a = gets.to_i
b = []
(1..100).each { |i|
  (1..100).each { |j|
    k = i + j
    b << i * j if k == a
  }
}
puts b.max

# 別解
a = gets.to_i
max = 0
(0..a).each { |x|
  y = a - x
  max = x * y if x * y > max
}
puts max
```
