- A問題（https://atcoder.jp/contests/abc172/tasks/abc172_a）
```
a = gets.to_i
puts a + a ** 2 + a ** 3
```

- B問題
```
s = gets.chomp
t = gets.chomp
cnt = 0
(0..s.size - 1).each { |i|
    cnt += 1 if s[i] != t[i]
}
puts cnt
```
