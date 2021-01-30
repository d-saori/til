- A問題
```
# 自分の解答(AC)
a, b, c = gets.split.map(&:to_i)
if c == 0 && a > b
  puts "Takahashi"
elsif c == 0 && a == b
  puts "Aoki"
elsif c == 0 && a < b
  puts "Aoki"
elsif c == 1 && a > b
  puts "Takahashi"
elsif c == 1 && a == b
  puts "Takahashi"
else c == 1 && a < b
  puts "Aoki"
end

# 別解
# C=0のとき、高橋くんが勝つ条件は A>B
# C=1のとき、高橋くんが勝つ条件は A>=B
a, b, c = gets.split.map(&:to_i)
puts a + c > b ? "Takahashi" : "Aoki"
```

- B問題
```
# 自分の解答(AC)
# s以下、d以上が効果あり呪文
n, s, d = gets.split.map(&:to_i)
cnt = 0
w = []
n.times {
  xy = gets.split.map(&:to_i)
  w << xy
}
w.each { |i|
  cnt += 1 if i[0] < s && i[1] > d
}
puts cnt >= 1 ? "Yes" : "No"

# 別解
n, s, d = gets.split.map(&:to_i)
n.times {
  x, y = gets.split.map(&:to_i)
  if x < s && y > d
    puts "Yes"
    exit
  end
}
puts "No"
```

- C問題
```

```
