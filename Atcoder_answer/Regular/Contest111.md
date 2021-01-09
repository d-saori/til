- A問題
```
n, m = gets.chomp.split.map(&:to_i)
puts 10 ** n / 2 % 2 #=> 少ない数値なら計算可
puts 10.pow(n, m) #=> may be too bigは出ないが先に余りの計算をしてしまう

# 解答
n, m = gets.chomp.split.map(&:to_i)
puts 10.pow(n, m ** 2) / m
```
