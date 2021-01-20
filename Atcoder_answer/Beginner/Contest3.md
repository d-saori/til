- A問題
```
n = gets.to_i
a = []
(1..n).each { |i|
  a << i * 10000
}
puts a.sum / n

# 別解
n = gets.to_i
puts (1..n).sum * 10**4 / n
```
