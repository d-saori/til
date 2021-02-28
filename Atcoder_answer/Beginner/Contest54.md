- A問題
```
a, b = gets.split.map(&:to_i)
if a > b && b != 1 || a == 1 && b != 1
  puts "Alice"
elsif b > a && a != 1 || b == 1 && a != 1
  puts "Bob"
else
  puts "Draw"
end

# 別解
# 1を14として扱う
a, b = gets.split.map(&:to_i)
a = 14 if a == 1
b = 14 if b == 1
if a == b
  puts "Draw"
elsif a > b
  puts "Alice"
else
  puts "Bob"
end
```

- B問題
```
n, m = gets.split.map(&:to_i)
a = n.times.map { gets.chomp }
b = m.times.map { gets.chomp }
cnt = 0
b.each_with_index { |b, i|
  cnt += 1 if a[i].include?(b)
}
puts cnt == m ? "Yes" : "No"
```
