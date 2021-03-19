- A問題
```
m, h = gets.split.map(&:to_i)
puts h % m == 0 ? "Yes" : "No"
```

- B問題
```
a, b, w = gets.split.map(&:to_f)
w = w * 1000
max = (w / a).floor
min = (w / b).ceil
puts max >= min ? [min, max].join(" ") : "UNSATISFIABLE"
```

- C問題
```
n = gets.to_i
x = 1000
ans = 0
while n >= x
  ans += n - x + 1
  x *= 1000
end
puts ans

# 別解
n = gets.to_i
ans = 0
ans += n - 999 if n >= 1000
ans += n - 999999 if n >= 1000000
ans += n - 999999999 if n >= 1000000000
ans += n - 999999999999 if n >= 1000000000000
ans += n - 999999999999999 if n >= 1000000000000000
puts ans
```
