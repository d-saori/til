- A問題（https://atcoder.jp/contests/abc106/tasks/abc106_a）

```
a, b = gets.split.map(&:to_i)

puts a * b - (a + b - 1)
```

- B問題（https://atcoder.jp/contests/abc106/tasks/abc106_b）
```
n = gets.to_i
# i % j = nの約数
puts (1..n).count { |i| 
  i.odd? && (1..i).count { |j|
    i % j == 0
  } == 8
}

もしくは
n = gets.to_i
ans = 0
(1..n).each { |i|
  # 奇数だけを配列に残す
  next if i % 2 == 0
  cnt = 0
  (1..i).each { |j|
    if i % j == 0
      cnt += 1
    end
    ans += 1 if cnt == 8
  }
}
puts ans
```
