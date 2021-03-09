- A問題
```
n, a, b = gets.split.map(&:to_i)
puts n - a + b
```

- B問題
```
n = gets.to_i
x = gets.split.map(&:to_i)
sum = 0
x.each { |i|
  sum += i.abs
}
puts sum

sum = 0
x.each { |i|
  sum += i ** 2
}
puts sum ** 0.5

puts x.max

# 別解
n = gets.to_i
x = gets.split.map(&:to_i).map(&:abs)
puts x.sum
puts x.map { |x| x ** 2 }.sum ** 0.5
puts x.max

# 別解
n = gets.to_i
x = gets.split.map(&:to_i)
m = []
y = []
(0..n-1).each { |i|
  m << (x[i]).abs
  y << (x[i]) ** 2
}
puts m.sum
puts (y.sum) ** 0.5
puts m.max
```

- C問題
```
n = gets.to_i
ans = []
i = 1
while i * i <= n
  if n % i == 0
    ans << i
    ans << n / i
  end
  i += 1
end
puts ans.uniq.sort
```
