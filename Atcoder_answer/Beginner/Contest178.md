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
abcd = gets.split.map(&:to_i)
x = abcd[0..1]
y = abcd[2..3]
ary = []
x.each { |i|
  y.each { |j|
    ary << i * j
  }
}
puts ary.max

# 別解
a, b, c, d = gets.split.map(&:to_i)
puts [a * c, a * d, b * c, b * d].max
```
