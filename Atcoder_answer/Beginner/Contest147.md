- A問題（https://atcoder.jp/contests/abc147/tasks/abc147_a）

```
a, b, c = gets.split.map(&:to_i)

if (a + b + c) >= 22
  puts "bust"
else
  puts "win"
end
```

- B問題
```
s = gets.chomp
n = s.size
cnt = 0
n.times { |i|
  j = n - 1 - i
  break if i >= j
  if s[i] != s[j]
    cnt += 1
  end
}
puts cnt

# 別解
s = gets.chomp.chars
puts s.count { |i| i != s.pop }
```
