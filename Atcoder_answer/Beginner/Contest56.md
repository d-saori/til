- A問題（https://atcoder.jp/contests/abc056/tasks/abc056_a）
```
a, b = gets.split
puts a == b ? "H" : "D"
```

- B問題
```
w, a, b = gets.split.map(&:to_i)
aa = [*a..a+w]
bb = [*b..b+w]
if aa.include?(bb[0])
  puts 0
elsif aa[-1] < bb[0]
  puts bb[0] - aa[-1]
else
  puts aa[0] - bb[-1]
end

# 別解
w, a, b = gets.split.map(&:to_i)
if (a - b).abs < w
  puts 0
else
  puts (a - b).abs - w
end
```
