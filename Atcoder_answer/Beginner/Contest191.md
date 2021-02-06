- A問題
```
v, t, s, d = gets.split.map(&:to_i)
puts v * t > d || v * (s - t) + v * t < d ? "Yes" : "No"
```

- B問題
```
n, x = gets.split.map(&:to_i)
a = gets.split.map(&:to_i)
a.delete_if { |i| i == x }
puts a.join(" ")
```

- C問題
```
h, w = gets.split.map(&:to_i)
s = h.times.map { gets.chomp.chars }
ans = 0
(0...h - 1).each { |i|
  (0..w - 1).each { |j|
    cnt = 0
    [[0, 0], [0, 1], [1, 0], [1, 1]].each { |n, m|
      cnt += 1 if s[i + n][j + m] == "#"
    }
    ans += 1 if cnt == 1 || cnt == 3
  }
}
puts ans
```
