- A問題（https://atcoder.jp/contests/abc155/tasks/abc155_a）

```
a, b, c = gets.split(" ").map(&:to_i)

if a == b && b == c
  puts "No"
elsif a == b || a == c || b == c
  puts "Yes"
else
  puts "No"
end

もしくは

nums = gets.split.map(&:to_i)
if nums.uniq.size == 2
  puts "Yes"
else
  puts "No"
end
```
