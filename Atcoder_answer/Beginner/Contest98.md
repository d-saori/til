- A問題（https://atcoder.jp/contests/abc098/tasks/abc098_a）

```
a, b = gets.split.map(&:to_i)
puts [a + b, a - b, a * b].max
```

- B問題
```
n = gets.to_i
s = gets.chomp.chars
cnt = []
(1..n-1).each { |i|
  t = s.dup
  u = t.shift(i)
  # &:双方に含まれる要素
  cnt << (t & u).size
}
puts cnt.max

# 別解
n = gets.to_i
s = gets.chomp.chars
cnt = []
(1..n-1).each { |i|
  cnt << (s[0..i] & s[i+1..-1]).count
}
puts cnt.max
```

- C問題
```
n = gets.to_i
s = gets.chomp.chars
left = 0
right = s.count("E")
ans = n
n.times { |i|
  t = 0
  curr = s[i]
  if curr == "W"
    t = left + right
    left += 1
  else
    right -= 1
    t = left + right
  end
  ans = t if t < ans
}
puts ans
```
