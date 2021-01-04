- A問題（https://atcoder.jp/contests/abc175/tasks/abc175_a）
  - 天気の組合せは、1,2,3日目がそれぞれ晴れ、雨かどうかで2**3=8通りしかないので、8通りの場合分けを書けば正答することができる。


```
S = gets.chomp

if S == "RRR"
  puts 3
elsif S == "SSS"
  puts 0
elsif S == "SSR" or S == "RRS"
  puts 2
else
  puts 1
end

# その他の回答
# 区切り文字に文字列を指定すると、その文字列の一致する部分で分割する
s = gets.chomp.split("S")
puts s.map(&:size).max.to_i
```

- B問題（https://atcoder.jp/contests/abc175/tasks/abc175_b）
```
n = gets.to_i
ary = gets.split.map!(&:to_i).sort!
# 三角形ができる条件：二辺の合計が一番長い辺より大きい

puts ary.combination(3).count { |a, b, c| a < b && b < c && (a + b > c)}
```
