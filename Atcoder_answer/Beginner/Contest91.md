- A問題（https://atcoder.jp/contests/abc091/tasks/abc091_a）
```
a, b, c = gets.split.map(&:to_i)
puts a + b >= c ? "Yes" : "No"
```

- B問題（https://atcoder.jp/contests/abc091/tasks/abc091_b）
```
# 青いカードに書かれた文字列それぞれについて、その文字列を言ったら何点貰えるかを計算し、その最大値を計算する
n = gets.to_i
blue = n.times.map { gets.chomp }
m = gets.to_i
red = m.times.map { gets.chomp }

ans = blue.uniq.map { |i| blue.count(i) - red.count(i) }.max
puts ans > 0 ? ans : 0
```
