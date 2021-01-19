- A問題
```
a = gets.to_i
# 相加相乗平均より、x = y = a / 2 の時 x * yが最大になる
x = a / 2
puts x * x

# 別解
a = gets.to_i
max = 0
(0..a).each { |x|
  y = a - x
  max = x * y if x * y > max
}
puts max
```
