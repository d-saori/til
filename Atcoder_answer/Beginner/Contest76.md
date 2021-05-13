- A問題
```
r, g = 2.times.map { gets.to_i }
puts 2 * g - r
```

- B問題
```
n, k = 2.times.map { gets.to_i }
x = 1
n.times {
  x = [x * 2, x + k].min
}
puts x

# 別解
n = gets.to_i
k = gets.to_i
ans = 1
n.times { |i|
  if ans * 2 >= ans + k
    ans += k
  else
    ans *= 2
  end
}
puts ans
```
