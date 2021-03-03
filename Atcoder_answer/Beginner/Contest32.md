- A問題
```
a, b, n = 3.times.map { gets.to_i }
min = a.lcm(b)
ans = min
while ans < n
  ans += min
end
puts ans
```

- B問題
```
s = gets.chomp.chars
k = gets.to_i
puts s.each_cons(k).uniq.size
```
