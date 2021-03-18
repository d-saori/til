- A問題（https://atcoder.jp/contests/abc151/tasks/abc151_a）

```
c = gets
puts c.succ

# 1行でも可
puts gets.succ

# nextメソッドもある
```

- B問題
```
n, k, m = gets.split.map(&:to_i)
a = gets.split.map(&:to_i)
if a.sum / n >= m
  puts 0
elsif a.sum / n <= m && m * n - a.sum <= k
  puts m * n - a.sum
else
  puts -1
end

# 別解
n, k, m = gets.split.map(&:to_i)
a = gets.split.map(&:to_i).sum
if a + k < n * m
  puts -1
else
  puts [n * m - a, 0].max
end
```

- C問題
```
n, m = gets.split.map(&:to_i)
ac = {}
wa = {}
wa_cnt = 0
m.times {
  p, s = gets.chomp.split
  if ac[p]
    next
  elsif s == "WA"
    wa[p] = (wa[p] || 0) + 1
  elsif s == "AC"
    ac[p] = "AC"
    wa_cnt += wa[p].to_i
  end
}
puts "#{ac.size} #{wa_cnt}"
```
