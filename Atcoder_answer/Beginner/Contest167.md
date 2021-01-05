- A問題（https://atcoder.jp/contests/abc167/tasks/abc167_a）

```
s = gets.chomp
t = gets.chomp
puts s[0..-1] == t[0..-2] ? "Yes" : "No"

もしくは
s = gets.chomp
t = gets.chomp
puts t.match?(/^#{s}.$/) ? 'Yes' : 'No'
```
