- A問題
```
a = gets.chomp
b = gets.chomp
puts a.reverse! == b ? "YES" : "NO"
```

- B問題
```
n = gets.to_i
(1..n).each { |i|
  if i ** 2 > n
    puts (i - 1) ** 2
    break
  end
}

# 別解
n = gets.to_i
# sqrtメソッド:非負整数 n の整数の平方根を返す(n の平方根以下の最大の非負整数を返す)
a = Math.sqrt(n).truncate
puts a ** 2
```
