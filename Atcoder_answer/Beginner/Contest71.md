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

# 別解
s = gets.chomp.chars.uniq.sort
("a".."z").each { |i|
  next if s.include?(i)
    puts i
    exit
}
puts "None"
```

- C問題
```
n = gets.to_i
a = gets.split.map(&:to_i).sort.reverse
e = []
i = 0
tmp = 0
while true
  break if i == a.size || e.size == 2
  if tmp == a[i]
    e << tmp if tmp == a[i]
    tmp = 0
  else
    tmp = a[i]
  end
  i += 1
end
res = 0
res = e[0] * e[1] if e.size == 2
puts res
```
