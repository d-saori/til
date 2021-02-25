- A問題
```
x, a, b = gets.split.map(&:to_i)
if b - a <= 0
  puts "deliciou"
else
  puts x >= b - a ? "safe" : "dangerous"
end

# 別解
x, a, b = gets.split.map(&:to_i)
if b > a && b - a <= x
  puts "safe"
elsif b > a && b - a >= x
  puts "dangerous"
else
  puts "delicious"
end
```

- B問題
```
n = gets.to_i
a = n.times.map { gets.to_i - 1 }
i = 0
n.times { |j|
  if i == 1
    puts j
    exit
  end
  i = a[i]
}
puts -1
```
