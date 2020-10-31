- A問題（https://atcoder.jp/contests/abc136/tasks/abc136_a）

```
a, b, c = gets.split.map(&:to_i)
ml = c - (a - b)
if ml <= 0
  puts 0
else
  puts ml
end

もしくは

a, b, c = gets.split.map(&:to_i)
puts [c - a + b, 0].max
```
