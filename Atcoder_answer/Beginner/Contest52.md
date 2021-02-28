- A問題
```
a, b, c, d = gets.split.map(&:to_i)
puts [a * b, c * d].max
```

- B問題
```
n = gets.to_i
s = gets.chomp.chars
x = 0
ary = []
n.times { |i|
  if s[i] == "I"
    ary << x += 1
  else
    ary << x -= 1
  end
}
puts [0, ary.max].max

# 別解
n = gets.to_i
s = gets.chomp.chars
x = 0
cnt = 0
n.times { |i|
  x += (s[i] == "I" ? 1 : -1)
  cnt = [cnt, x].max
}
puts cnt
```
