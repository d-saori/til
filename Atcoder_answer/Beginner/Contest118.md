- A問題（https://atcoder.jp/contests/abc118/tasks/abc118_a）

```
a, b = gets.split.map(&:to_i)

if b % a == 0
  puts a + b
else
  puts b - a
end
```
