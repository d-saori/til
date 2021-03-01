- A問題
```
s = gets.chomp.split
sa = s[0]
sb = s[1]
sc = s[2]
puts "#{sa[0, 1]}#{sb[0, 1]}#{sc[0, 1]}"

# 別解
s = gets.chomp.split
puts s[0][0] + s[1][0] + s[2][0]
```

- B問題
```
a, b, x = gets.split.map(&:to_i)
i = b / x
j = a / x
ans = i - j
ans += 1 if a % x == 0
puts ans
```
