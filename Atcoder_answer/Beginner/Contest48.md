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
