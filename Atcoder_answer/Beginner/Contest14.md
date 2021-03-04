- A問題
```
a, b = 2.times.map { gets.to_i }
puts a % b == 0 ? 0 : b - a % b
```

- B問題
```
n, x = gets.split.map(&:to_i)
a = gets.split.map(&:to_i)
ans = 0
x.to_s(2).chars.reverse.each_with_index { |c, i|
  ans += a[i] if c == "1"
}
puts ans
```
