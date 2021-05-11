- A問題（https://atcoder.jp/contests/abc078/tasks/abc078_a）
```
x, y = gets.split
# if x < y
#   puts "<"
# elsif x > y
#   puts ">"
# else
#   puts "="
# end
puts x == y ? "=" : x > y ? ">" : "<"
```

- B問題（https://atcoder.jp/contests/abc078/tasks/abc078_b）
```
x, y, z = gets.split.map(&:to_i)
ans = 0
while true
  if (y * ans + z * (ans + 1)) > x
    break
  end
  ans += 1
end
puts ans - 1

# 別解
x, y, z = gets.split.map(&:to_i)
sum = y + (z * 2)
cnt = 0
while sum <= x
  sum += y + z
  cnt += 1
end
puts cnt

# 別解
x, y, z = gets.split.map(&:to_i)
puts (x - z) / (y + z)
```

- C問題
```
n, m = gets.split.map(&:to_i)
k = 1
m.times {
  k *= 2
}
puts ((n - m) * 100 + 1900 * m) * k
```
