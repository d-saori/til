- A問題（https://atcoder.jp/contests/abc064/tasks/abc064_a）

```
r, g, b = gets.split
if (r + g + b).to_i % 4 == 0
  puts "YES"
else
  puts "NO"
end

# 簡略化
if gets.split.join.to_i % 4 == 0
  puts "YES"
else
  puts "NO"
end
```
