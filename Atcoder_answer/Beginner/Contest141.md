- A問題（https://atcoder.jp/contests/abc141/tasks/abc141_a）

```
s = gets.chomp
if s == "Sunny"
  puts "Cloudy"
elsif s == "Cloudy"
  puts "Rainy"
else
  puts "Sunny"
end

もしくは

s = %w(Sunny Cloudy Rainy)
puts s[s.index(gets.chomp) - 2]
```

- B問題
```
s = gets.chomp.chars
odd = s.select.with_index { |_, i| i.even? }
even = s.select.with_index { |_, i| i.odd? }
puts odd.each.count { |i| "RUD".include?(i) } + even.each.count { |j| "LUD".include?(j) } == s.size ? "Yes" : "No"
```

- C問題
```
n, k, q = gets.split.map(&:to_i)
a = q.times.map { gets.to_i }
# n人全てのポイントからq回分のポイントを引いておく
ary = [k-q] * n
# 正解した人にポイントを足していく
q.times { |i|
  ary[a[i]-1] += 1
}
ary.each { |j|
  puts j <= 0 ? "No" : "Yes"
}
```
