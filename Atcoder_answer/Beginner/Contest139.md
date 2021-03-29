- A問題（https://atcoder.jp/contests/abc139/tasks/abc139_a）
```
s = gets.to_s
t = gets.to_s
count = 0

(0..2).each do |i|
  count += 1 if s[i] == t[i]
end

puts count
```

- B問題
```
a, b = gets.split.map(&:to_i)
cnt = 0
sum = 1
while sum < b
  sum += a - 1
  cnt += 1
end
puts cnt

# 別解
a, b = gets.split.map(&:to_i)
puts ((b - 1) / (a - 1).to_f).ceil
```

- C問題
```
n = gets.to_i
h = gets.split.map(&:to_i)
cnt = 0
ans = 0
h.each_cons(2) { |a, b|
  if a >= b
    cnt += 1
  else
    cnt = 0
  end
  ans = [ans, cnt].max
}
puts ans

# 別解
n = gets.to_i
h = gets.split.map(&:to_i)
a = h.slice_when { |i, j| i < j }
b = []
a.each { |i|
  b << i.size - 1
}
puts b.max

# 別解
n = gets.to_i
h = gets.split.map(&:to_i)
m = h.slice_when { |a, b| a < b }
puts (m.map(&:size).max - 1)
```

- D問題
```
n = gets.to_i
# 1から(n-1)の和を求める
puts n * (n - 1) / 2
```
