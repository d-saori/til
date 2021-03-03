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

- B問題
```
n = gets.to_i
r = n.times.map { gets.to_i }.sort.reverse
red = []
white = []
(0..n-1).each { |i|
  if i.even?
    red << r[i]
  else
    white << r[i]
  end
}
a = []
b = []
red.each { |r| 
  a << (r ** 2) * Math::PI
}
white.each { |w|
  b << (w ** 2) * Math::PI
}
puts a.sum - b.sum

# 別解
n = gets.to_i
r = n.times.map { gets.to_i }.sort.reverse
ans = 0
r.each_slice(2).each { |red, white|
  ans += red ** 2 if red
  ans -= white ** 2 if white
}
puts ans * Math::PI
```
