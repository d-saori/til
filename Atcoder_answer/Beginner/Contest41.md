- A問題
```
s = gets.chomp
t = gets.to_i
puts s[t - 1]
```

- B問題
```
a, b, c = gets.split.map(&:to_i)
puts (a * b * c) % (10 ** 9 + 7)
```
