- A問題
```
a, d = gets.split.map(&:to_i)
puts [(a + 1) * d, a * (d + 1)].max
```

- B問題
```
l, h = gets.split.map(&:to_i)
n = gets.to_i
a = n.times.map { gets.to_i }
a.each { |i|
  if l <= i && i <= h
    puts 0
  elsif i >= h
    puts -1
  else
    puts l - i
  end
}

# 別解
l, h = gets.split.map(&:to_i)
n = gets.to_i
n.times {
  a = gets.to_i
  puts h < a ? -1 : [l - a, 0].max
}
```
