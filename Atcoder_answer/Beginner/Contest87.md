- A問題
```
x, a, b = 3.times.map { gets.to_i }
puts (x - a) % b
```

- B問題
```
a, b, c, x = 4.times.map { gets.to_i }
cnt = 0
(0..a).each { |i|
  (0..b).each { |j|
    (0..c).each { |k|
      cnt += 1 if 500 * i + 100 * j + 50 * k == x
    }
  }
}
puts cnt

# 別解
a, b, c, x = 4.times.map { gets.to_i }
cnt = 0
(0..a).each { |i|
  (0..b).each { |j|
    n = x - 500 * i - 100 * j
    cnt += 1 if n >= 0 && n <= 50 * c
  }
}
puts cnt
```

- C問題
```
# 移動方法は、右にi回、下に1回、右にn-i回
n = gets.to_i
a = 2.times.map { gets.split.map(&:to_i) }
(1..n-1).each { |i|
  a[0][i] += a[0][i-1]
  a[1][n-1-i] += a[1][n-i]
}
m = 0
(0..n-1).each { |i|
  m = [m, a[0][i] + a[1][i]].max
}
puts m
```
