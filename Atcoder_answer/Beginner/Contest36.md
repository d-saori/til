- A問題
```
a, b = gets.split.map(&:to_i)
puts b % a == 0 ? b / a : b / a + 1
```

- B問題
```
n = gets.to_i
s = n.times.map { gets.chomp.chars }
s.transpose.each { |i|
  puts i.reverse.join
}
```
