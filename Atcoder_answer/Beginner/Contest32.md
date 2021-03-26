- A問題
```
a, b, n = 3.times.map { gets.to_i }
ans = 0
while
  if n % a == 0 && n % b == 0
    ans = n
    break
  end
  n += 1
end
puts ans

# 別解
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
