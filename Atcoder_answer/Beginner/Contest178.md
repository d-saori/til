- A問題（https://atcoder.jp/contests/abc178/tasks/abc178_a）

```
x = gets.to_i
if x == 0
  puts 1
else
  puts 0
end

# 三項演算子
x = gets.to_i
puts x == 0 ? 1 : 0
```

- B問題
```
a, b, c, d = gets.split.map(&:to_i)
puts [a * c, a * d, b * c, b * d].max
```
