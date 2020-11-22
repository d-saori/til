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
