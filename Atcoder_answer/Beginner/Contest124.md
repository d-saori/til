- A問題（https://atcoder.jp/contests/abc124/tasks/abc124_a）

```
a, b = gets.split.map(&:to_i)

if a > b
  puts (a * 2) - 1
elsif a < b
  puts (b * 2) - 1
else
  puts a + b
end

もしくは
if a == b
  puts a + b
else
  r = [a, b].max
  puts r + r - 1
end
```

- B問題
```
n = gets.to_i
h = gets.split.map(&:to_i)
cnt = 0
max = 0
h.each { |i|
  if max <= i
    cnt += 1
    max = i
  end
}
puts cnt

# 別解
n = gets.to_i
h = gets.split.map(&:to_i)
puts n.times.count { |i| h[0..i].max == h[i] }
```

- C問題
```
s = gets.chomp
cnt = 0
s.size.times { |i|
  cnt += 1 if i % 2 != s[i].to_i
}
puts [cnt, s.size - cnt].min
```
