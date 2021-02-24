- A問題
```
a, b = gets.split.map(&:to_i)
puts a * b % 2 == 0 ? "Even" : "Odd"
```

- B問題
```
a, b = gets.chomp.split
n = (a + b).to_i
m = (n ** (1 / 2.0)).floor
puts m ** 2 == n ? "Yes" : "No"

# 別解
a, b = gets.chomp.split
n = (a + b).to_i
m = Math.sqrt(n).to_i
puts m ** 2 == n ? "Yes" : "No"
```
