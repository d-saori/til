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
