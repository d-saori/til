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
