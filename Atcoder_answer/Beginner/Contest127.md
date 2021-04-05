- A問題（https://atcoder.jp/contests/abc127/tasks/abc127_a）

```
a, b = gets.split.map(&:to_i)

if a >= 13
  puts b
elsif a <= 5 
  puts 0
else
  puts b / 2
end
```

- B問題
```
r, d, x = gets.split.map(&:to_i)
10.times {
  x = r * x - d
  puts x
}

# 別解
r, d, x = gets.split.map(&:to_i)
10.times {
  a = r * x - d
  puts a
  x = a
}

# 別解
r, d, x = gets.split.map(&:to_i)
(1..10).each { |i|
  puts r * x - d
  x = r * x - d
}
```
