- A問題（https://atcoder.jp/contests/abc133/tasks/abc133_a）

```
n, a, b = gets.split.map(&:to_i)
r = n * a

puts [r, b].min

と回答しACだったが、変数rの下りはいらず

n, a, b = gets.split.map(&:to_i)

puts [n * a, b].min

でOK
```
