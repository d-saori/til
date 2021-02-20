- A問題（https://atcoder.jp/contests/abc115/tasks/abc115_a）

```
d = gets.to_i
if d == 25
  puts "Christmas"
elsif d == 24
  puts "Christmas Eve"
elsif d == 23
  puts "Christmas Eve Eve"
else d == 22
  puts "Christmas Eve Eve Eve"
end

# 別解
d = gets.to_i
puts "Christmas" + "Eve" * (25 - d)
```

- B問題
```
n = gets.to_i
p = n.times.map { gets.to_i }.sort.reverse
puts p[0] / 2 + p[1..-1].sum

# 別解
n = gets.to_i
p = n.times.map { gets.to_i }
puts p.sum - p.max / 2
```
