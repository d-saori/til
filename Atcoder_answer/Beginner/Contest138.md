- A問題（https://atcoder.jp/contests/abc138/tasks/abc138_a）
```
a = gets.to_i
s = gets.to_s

if a >= 3200
  puts s
else
  puts "red"
end
```

- B問題（https://atcoder.jp/contests/abc138/tasks/abc138_b）
```
n = gets.to_i
a = gets.split.map(&:to_i)
b = []
a.each { |i|
  b << 1 / i.to_f
}
puts 1 / b.sum

# 別解
n = gets.to_i
a = gets.split.map(&:to_f)
sum = 0
a.each { |i|
  sum += 1 / i
}
puts 1.0 / sum

# 別解
n = gets.to_i
a = gets.split.map(&:to_i)
sum = a.map { |i| 1.0 / i }.sum
puts 1 / sum
```

- C問題
```
# 小さい数字ほど多く割られるようにしておけば最終値は最大値になる
n = gets.to_i
v = gets.split.map(&:to_f).sort
(n-1).times {
  x = v.shift
  y = v.shift
  v.unshift((x + y) / 2)
}
puts v.first

# 別解
n = gets.to_i
v = gets.split.map(&:to_f).sort!
a = v.shift
v.each { |i|
  a = (a + i.to_f) / 2
}
puts a
```
