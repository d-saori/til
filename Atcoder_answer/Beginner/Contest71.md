- A問題
```
x, a, b = gets.split.map(&:to_i)
if (b - x).abs > (a - x).abs
  puts "A"
else
  puts "B"
end
```

- B問題
```
s = gets.chomp.chars
ans = "None"
# !:unlessと同意
("a".."z").each { |i|
  if !s.include?(i)
    puts i
    exit
  end
}
puts ans
```
