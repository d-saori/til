- A問題（https://atcoder.jp/contests/abc137/tasks/abc137_a）
```
a, b = gets.split.map(&:to_i)
puts [a + b, a - b, a * b].max
```

- B問題
```
k, x = gets.split.map(&:to_i)
min = x - k + 1
max = x + k - 1
puts (min..max).to_a.join(" ")
```

- C問題
```
n = gets.to_i
s = n.times.map { gets.chomp.chars.sort.join }.tally
ans = 0
s.values.each { |i| ans += i * (i - 1) / 2 }
puts ans

# 別解
n = gets.to_i
s = n.times.map { gets.chomp.chars.sort.join }
puts s.tally.sum { |_, cnt| cnt * (cnt - 1) / 2 }

# 別解
n = gets.to_i
s = n.times.map { gets.chomp.chars.sort.join }
puts s.group_by(&:itself).map { |i, j| j.combination(2).size }.sum

# 別解
n = gets.to_i
h = Hash.new(0)
ans = 0
n.times {
  s = gets.chomp.chars.sort.join
  ans += h[s] if h[s] > 0
  h[s] += 1
}
puts ans
```
