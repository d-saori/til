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

- B問題
```
s, t = 2.times.map { gets.chomp }
c = "atcoder".chars
if s.chars.zip(t.chars).all? { |i, j| i == j || (i == "@" && c.include?(j)) || (j == "@" && c.include?(i)) }
  puts "You can win"
else
  puts "You will lose"
end
```
