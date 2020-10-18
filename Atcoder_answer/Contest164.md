- A問題（https://atcoder.jp/contests/abc164/tasks/abc164_a）

```
s, w = gets.chomp.split(" ").map(&:to_i)

if s <= w
  puts "unsafe"
else
  puts "safe"
end
```
