- A問題（https://atcoder.jp/contests/abc060/tasks/abc060_a）
```
a, b, c = gets.split
puts a[-1] == b[0] && b[-1] == c[0] ? "YES" : "NO"
```

- B問題
```
a, b, c = gets.split.map(&:to_i)
(1..100).each { |i|
  if a * i % b == c
    puts "YES"
    exit
  end
}
puts "NO"
```
