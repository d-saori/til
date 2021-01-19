- A問題
```
a, b, c, k = gets.split.map(&:to_i)
s, t = gets.split.map(&:to_i)
puts s + t >= k ? s * a + t * b - (s + t) * c : s * a + t * b
```
