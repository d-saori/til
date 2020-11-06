- A問題（https://atcoder.jp/contests/abc114/tasks/abc114_a）

```
x = gets.to_i

if x == 3 || x == 5 || x == 7
  puts "YES"
else
  puts "NO"
end

または
if [7,5,3].include? x
  puts "YES"
else
  puts "NO"
end
などでもOK
```
