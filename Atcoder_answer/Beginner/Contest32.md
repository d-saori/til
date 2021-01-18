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
