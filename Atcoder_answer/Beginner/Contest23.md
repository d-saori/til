- A問題
```
x = gets.to_i
puts x / 10 + (x - x / 10 * 10)
```

- B問題
```
n = gets.to_i
s = gets.chomp
ans = -1
if n.odd?
  t = "b"
  (1..(n - 1) / 2).each { |i|
    t = "a" + t + "c" if (i % 3) == 1
    t = "c" + t + "a" if (i % 3) == 2
    t = "b" + t + "b" if (i % 3) == 0
  }
  ans = (n - 1) / 2 if s == t
end
puts ans
```
