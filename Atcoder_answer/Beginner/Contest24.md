- A問題
```
a, b, c, k = gets.split.map(&:to_i)
s, t = gets.split.map(&:to_i)
puts s + t >= k ? s * a + t * b - (s + t) * c : s * a + t * b
```

- B問題
```
n, t = gets.split.map(&:to_i)
ans = 0
pre = 0
n.times {
  now = gets.to_i
  if pre <= now
    ans += t
    pre = now + t
  else
    ans += t - (pre - now)
    pre = now + t
  end
}
puts ans
```
