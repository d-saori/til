- A問題（https://atcoder.jp/contests/abc051/tasks/abc051_a）
```
s = gets.split(",")
puts s.join(" ")
```

- B問題
```
k, s = gets.split.map(&:to_i)
cnt = 0
(0..k).each { |x|
  (0..k).each { |y|
  z = s - x - y
  cnt += 1 if 0 <= z && z <= k
  }
}
puts cnt
```
