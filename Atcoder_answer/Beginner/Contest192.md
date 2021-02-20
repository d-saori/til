- A問題
```
x = gets.to_i
puts x % 100 == 0 ? 100 : (x / 100.to_f).ceil * 100 - x
```

- B問題
```
s = gets.chomp
odd = [] 
even = [] 
s.each_char.with_index { |c, index|
  odd << c if index % 2 == 0
}
s.each_char.with_index { |c, index|
  even << c if index % 2 != 0
}
s = ["A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z"]
o = ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z"]
puts odd.all? { |i| o.include?(i) } && even.all? { |j| s.include?(j) } ? "Yes" : "No"

# 別解
s = gets.chomp
cnt = 0
(0..s.size-1).each { |i|
  if i.even?
    cnt += 1 if s[i] != s[i].downcase
  else
    cnt += 1 if s[i] == s[i].downcase
  end
}
puts cnt > 0 ? "No" : "Yes"
```

- C問題
```
n, k = gets.split.map(&:to_i)
s = [n.to_s]
k.times { |i|
  a = s[i].to_s.chars.sort.reverse.join.to_i - s[i].to_s.chars.sort.join.to_i
  s << a
}
puts s[-1]
```

- D問題
```
# REで不正解だったコード
x = gets.chomp
m = gets.to_i
d = x.chars.max.to_i + 1
num = 0
s = []
while num < m
  num = x.to_i(d)
  s << num
  d += 1
end
puts s.select { |i| i <= m }.count

# 正解

```
