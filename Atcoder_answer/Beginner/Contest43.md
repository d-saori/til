- A問題
```
n = gets.chomp.to_i
a = []
(1..n).each { |i|
  a << i
}
puts a.sum

# 別解
n = gets.chomp.to_i
p (1..n).sum
```

- B問題
```
s = gets.chomp.chars
w = []
s.each { |i|
  if i == "B"
    w.pop
  else
    w << i
  end
}
puts w.join
```
