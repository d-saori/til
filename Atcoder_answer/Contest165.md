- A問題（https://atcoder.jp/contests/abc165/tasks/abc165_a）

```
k = gets.chomp.to_i
a, b = gets.chomp.split(" ").map(&:to_i)

if (b/k)*k >= a
  puts "OK"
else 
  puts "NG"
end
```
