- A問題
```
n = gets.to_i
puts n / 3
```

- B問題
```
n = gets.to_i
s = gets.chomp.split
t = []
s.each { |i|
  t << i
}
puts t.uniq.size == 3 ? "Three" : "Four"

# 別解
n = gets.to_i
s = gets.chomp.split
puts s.index("Y") ? "Four" : "Three"
```
