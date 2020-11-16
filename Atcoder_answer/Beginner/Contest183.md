- A問題（https://atcoder.jp/contests/abc183/tasks/abc183_a）

```
x = gets.to_i
if x >= 0
  puts x
else
  puts 0
end
```

- B問題（https://atcoder.jp/contests/abc183/tasks/abc183_b）

```
a, b, c, d = gets.split.map(&:to_f)
puts ((a * d) + (c * b)) / (b + d)
```
