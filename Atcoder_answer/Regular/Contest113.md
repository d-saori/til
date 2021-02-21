- A問題
```
k = gets.to_i
cnt = 0
(1..k).each { |i|
  s = k / i
  (1..s).each { |j|
    cnt += s / j
  }
}
puts cnt

# 別解
k = gets.to_i
cnt = 0
(1..k).each { |i|
  (1..k/i).each { |j|
    cnt += k / i / j
  }
}
puts cnt
```
