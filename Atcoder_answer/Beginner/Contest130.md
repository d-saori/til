- A問題（https://atcoder.jp/contests/abc130/tasks/abc130_a）

```
x, a = gets.split.map(&:to_i)
puts x < a ? 0 : 10
```

- B問題
```
n, x = gets.split.map(&:to_i)
l = gets.split.map(&:to_i)
cnt = 1
sum = 0
(0..n-1).each { |i|
  sum = sum + l[i]
  cnt += 1 if sum <= x
}
puts cnt

# 別解
n, x = gets.split.map(&:to_i)
l = gets.split.map(&:to_i)
cnt = 1
sum = 0
l.each { |i|
  sum += i
  cnt += 1 if sum <= x
}
puts cnt

# 別解
n, x = n, x = gets.split.map(&:to_i)
l = gets.split.map(&:to_i)
sum = 0
puts l.map { |i| sum += i }.count { |j| j <= x } + 1
```

- C問題
```
# 指定された座標と長方形の中心点を結んだ直線で分けると面積を半分にできる
# 指定された点が中心点の時は直線は複数ある
# 上記のような直線が何本あるか求める
w, h, x, y = gets.split.map(&:to_f)
s = (w * h) / 2
flag = (x == w / 2) && (y == h / 2) ? 1 : 0
puts [s, flag].join(" ")
```
