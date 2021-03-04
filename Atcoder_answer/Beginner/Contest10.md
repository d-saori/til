- A問題
```
s = gets.chomp
puts s + "pp"
```

- B問題
```
n = gets.to_i
a = gets.split.map(&:to_i)
cnt = 0
a.each { |i|
  while i % 2 == 0 || i % 5 == 0
    i -= 1
    cnt += 1
  end
}
puts cnt
```
