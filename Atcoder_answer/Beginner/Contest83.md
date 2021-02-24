- A問題
```
a, b, c, d = gets.split.map(&:to_i)
if a + b > c + d
  puts "Left"
elsif a + b < c + d
  puts "Right"
else
  puts "Balanced"
end
```

- B問題
```
n, a, b = gets.split.map(&:to_i)
ary = []
(1..n).each { |i|
  t = i.digits.sum
  ary << i if a <= t && t <= b
}
puts ary.sum
```
