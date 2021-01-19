- A問題
```
s = gets.chomp.chars
n = gets.chomp.to_i
r = s.repeated_permutation(2).to_a
puts r[n - 1].join

# 別解
s = gets.chomp.chars
n = gets.chomp.to_i
puts s.product(s)[n - 1].join
```
