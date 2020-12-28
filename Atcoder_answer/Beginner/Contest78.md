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

もしくは
x, y, z = gets.split.map(&:to_i)
puts (x - z) / (y + z)
```
