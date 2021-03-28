- A問題
```
s = gets.chomp.chars
puts s.rotate.join
```

- B問題
```
h, w, x, y = gets.split.map(&:to_i)
s = h.times.map { gets.chomp.chars }
cnt = 1 #=> 始点を含むので1
# 上方向
(y + 1).upto(w) { |i|
  t = s[x - 1][i - 1]
  break if t.eql?("#")
  cnt += 1
}
# 下方向
(y - 1).downto(1) { |i|
  t = s[x - 1][i - 1]
  break if t.eql?("#")
  cnt += 1
}
# 左方向
(x - 1).downto(1) { |i|
  t = s[i - 1][y - 1]
  break if t.eql?("#")
  cnt += 1
}
# 右方向
(x + 1).upto(h) { |i|
  t = s[i - 1][y - 1]
  break if t.eql?("#")
  cnt += 1
}
puts cnt

# 別解xとy逆に入力している
h, w, y, x = gets.split.map(&:to_i)
fields = h.times.map { gets.chomp.chars }
ans = 0
# ある始点から上下左右に行けるまで行ってマス目を数える
[[0, 1], [0, -1], [-1, 0], [1, 0]].each { |dx, dy|
  x_c = x
  y_c = y
  while true
    x_c += dx
    y_c += dy
    break if x_c < 1 || x_c > w || y_c < 1 || y_c > h || fields[y_c - 1][x_c - 1] == "#"
    ans += 1
  end
}
puts ans + 1
```
