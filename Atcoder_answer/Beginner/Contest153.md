- A問題（https://atcoder.jp/contests/abc153/tasks/abc153_a）

```
h, a = gets.chomp.split.map(&:to_i)
puts (h / a.to_f).ceil

# 別解
h, a = gets.split.map(&:to_i)
ans = 0
while true
  h -= a
  ans += 1
  if h <= 0
    puts ans
    break
  end
end

# 別解
h, a = gets.split.map(&:to_i)
puts h % a == 0 ? h / a : h / a + 1
```

- B問題
```
h, n = gets.split.map(&:to_i)
a = gets.split.map(&:to_i)
puts a.sum >= h ? "Yes" : "No"
```

- C問題
```
n, k = gets.split.map(&:to_i)
h = gets.split.map(&:to_i)
ans = 0
if h.size == k || h.size < k
  puts 0
elsif k == 0
  h.each { |i| ans += i }
  puts ans
else
  m = h.sort.reverse
  m.shift(k)
  m.each { |i| ans += i }
  puts ans
end

# 別解
n, k = gets.split.map(&:to_i)
h = gets.split.map(&:to_i).sort
h.pop(k)
puts h.empty? ? 0 : h.sum
```
