- A問題（https://atcoder.jp/contests/abc115/tasks/abc115_a）

```
d = gets.to_i

if d == 25
  puts "Christmas"
elsif d == 24
  puts "Christmas Eve"
elsif d == 23
  puts "Christmas Eve Eve"
else d == 22
  puts "Christmas Eve Eve Eve"
end

より
d = gets.to_i

puts "Christmas" + "Eve" * (25 - d)
```
