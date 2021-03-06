- A問題（https://atcoder.jp/contests/abc184/tasks/abc184_a）
```
a, b = gets.split(" ").map(&:to_i)
c, d = gets.split(" ").map(&:to_i)
puts a * d - b * c
```

- B問題（https://atcoder.jp/contests/abc184/tasks/abc184_b）
```
# 自分の解答（不正解）
a, b = gets.split(" ").map(&:to_i)
s = gets.chomp.split("") #=> 入力xoxなら["x", "o", "x"]

s_o = s.count("o")
s_x = s.count("x")

if b == 0
  puts (s_o * 1 + s_x * -1) + 1
elsif s_o * 1 + s_x * -1 <= 0
  puts 0
else
  puts (s_o * 1 + s_x * -1) + b
end

# 正解答
a, b = gets.split(" ").map(&:to_i)
s = gets.chomp.split("")

ans = b
a.times do |i|
  if s[i] == "o"
    ans += 1
  else
    ans -= 1
    if ans < 0
      ans = 0
    end
  end
end

ans = 0 if ans < 0
p ans
```

- C問題
```
r1, c1 = gets.split.map(&:to_i)
r2, c2 = gets.split.map(&:to_i)
# 移動a : r1 + c1 == r2 + c2
# 移動b : r1 - c1 == r2 - c2
# 移動c : (r1 - c1).abs + (r2 - c2).abs <= 3
# 斜め移動は同じ色のマスしか行けないので、斜め移動(移動a,b)1〜2回とその他の移動(移動c)の3手は必ずできる
# 0, 1, 2の判定をすればいい
# 0手 : 一致
# 1手 : 問題通り
# 2手 : AB, AC, BC, CC
x = (r1 - r2).abs
y = (c1 - c2).abs
z = x + y
if z == 0
  puts 0
elsif z <= 3 || x == y
  puts 1
elsif z <= 6 || z.even? || (x - y).abs <= 3
  puts 2
else
  puts 3
end
```
