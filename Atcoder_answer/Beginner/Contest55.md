- A問題
```
n = gets.to_i
puts n >= 15 ? n * 800 - 200 * (n / 15) : n * 800
```

- B問題
```
n = gets.to_i
mod = 10 ** 9 + 7
puts (1..n).inject(1) { |a, i| a * i % mod}

# 別解
n = gets.to_i
mod = 10 ** 9 + 7
a = 1
(1..n).each { |i|
  a = a * i % mod
}
puts a
```
