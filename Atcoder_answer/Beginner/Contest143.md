- A問題（https://atcoder.jp/contests/abc143/tasks/abc143_a）

```
a, b = gets.split.map(&:to_i)

if a > b * 2
  puts a - b * 2
else
  puts 0
end

もしくは

a, b = gets.split.map(&:to_i)
puts [0, a - b * 2].max
```

- B問題
```
n = gets.to_i
d = gets.split.map(&:to_i)
tako = []
d.combination(2).map { |i, j|
  tako << i * j
}
puts tako.sum

# 別解
n = gets.to_i
d = gets.split.map(&:to_i)
puts d.combination(2).map { |i, j| i * j }.sum
```
