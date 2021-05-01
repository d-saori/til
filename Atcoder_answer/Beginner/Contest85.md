- A問題（https://atcoder.jp/contests/abc085/tasks/abc085_a）
```
s = gets
puts s.gsub(/2017/, "2018")
```

- B問題
```
n = gets.to_i
d = n.times.map { gets.to_i }.sort
puts d.uniq.size
```

- C問題
```
n, y = gets.split.map(&:to_i)
key = 0
(0..n).each { |i|
  break if y > n * 10000
  break if y < i * 10000
  (0..(n - i)).each { |j|
    break if y > i * 10000 + (n - i) * 5000
    k = n - i - j
    break if y < i * 10000 + j * 5000 + k * 1000
    if y == (i * 10000 + j * 5000 + k * 1000)
      puts [i, j, k].join(" ")
      key = 1
      break
    end
  }
  break if key == 1
}
puts "-1 -1 -1" if key == 0
```
