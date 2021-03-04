- A問題
```
n = gets.chomp
puts n.include?("3") || n.to_i % 3 == 0 ? "YES" : "NO"
```

- B問題
```
n = gets.to_i
a = [0, 0, 1]
(3..n).each { |i|
  a << (a[i - 1] + a[i - 2] + a[i - 3]) % 10007
}
puts a[n - 1]
```
