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
# それぞれの人がどちらの皿にボールを置くかの 2**K通り を全探索
# それぞれの人がどちらの皿にボールを置くかを固定したとき、満たされる条件の個数は O(N+M+K)で求めることができる
n, m = gets.split.map(&:to_i)
ab = m.times.map { gets.split.map(&:to_i) }
k = gets.to_i
cd = m.times.map { gets.split.map(&:to_i) }

max = 0
(0..2**k-1).each { |i|
  sara = {}
  (0..k-1).each { |j|
    sara[cd[j][(i >> j) & 1]] = true
  }
  sum = 0
  ab.each { |p|
    sum += 1 if sara[p[0]] && sara[p[1]]
  }
  ans = sum if sum > max
}
puts max
```
