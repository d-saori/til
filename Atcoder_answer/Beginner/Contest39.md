- A問題
```
a, b, c = gets.split.map(&:to_i)
puts 2 * (b * c + b * a + c * a)
```

- B問題
```
x = gets.to_i
(1..10**9).each { |i|
  if i ** 4 == x
    puts i
    break
  end
}

# 別解
x = gets.to_i
puts x ** (1.0 / 4)
```
