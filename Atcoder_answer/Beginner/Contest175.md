- A問題（https://atcoder.jp/contests/abc175/tasks/abc175_a）
  - 天気の組合せは、1,2,3日目がそれぞれ晴れ、雨かどうかで2**3=8通りしかないので、8通りの場合分けを書けば正答することができる。


```
s = gets.chomp
if s == "RRR"
  puts 3
elsif s == "RRS" || s == "SRR"
  puts 2
elsif s == "RSS" || s == "RSR" || s == "SSR" || s == "SRS"
  puts 1
else
  puts 0
end

# 別解1
# 区切り文字に文字列を指定すると、その文字列の一致する部分で分割する
s = gets.chomp.split("S")
puts s.map(&:size).max.to_i

# 別解2
s = gets.chomp
puts s == "RSR" ? 1 : s.count("R")
```

- B問題（https://atcoder.jp/contests/abc175/tasks/abc175_b）
```
# 三角形ができる条件：二辺の合計が一番長い辺より大きい
n = gets.to_i
l = gets.split.map(&:to_i).sort
p l.combination(3).count { |i, j, k| i < j && j < k && i + j > k }

# 別解
n = gets.to_i
l = gets.split.map(&:to_i).sort
cnt = 0
l.combination(3).each { |a, b, c|
  # cnt += 1 if a < b + c && b < a + c && c < a + b && a != b && b != c && c != a
  cnt += 1 if a < b && b < c && a + b > c
}
puts cnt
```

- C問題
```
x, k, d = gets.split.map(&:to_i)
x = x.abs
move = [k, x / d].min
k -= move
x -= move * d
puts k.even? ? x : (x - d).abs
```
