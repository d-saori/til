- A問題（https://atcoder.jp/contests/abc167/tasks/abc167_a）

```
s = gets.chomp
t = gets.chomp

if s == t[0, s.size]
  puts 'Yes'
else
  puts 'No'
end

s = gets.chomp
t = gets.chomp

puts t.match?(/^#{s}.$/) ? 'Yes' : 'No'
```
