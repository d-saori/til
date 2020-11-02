- A問題（https://atcoder.jp/contests/abc124/tasks/abc124_a）

```
a, b = gets.split.map(&:to_i)

if a > b
  puts (a * 2) - 1
elsif a < b
  puts (b * 2) - 1
else
  puts a + b
end

もしくは
if a == b
  puts a + b
else
  r = [a, b].max
  puts r + r - 1
end
```
