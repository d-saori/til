- A問題（https://atcoder.jp/contests/abc187/tasks/abc187_a）
```
a, b = gets.split
a_sum = a.chars.map(&:to_i).sum
b_sum = b.chars.map(&:to_i).sum
puts [a_sum, b_sum].max
```

- B問題（https://atcoder.jp/contests/abc187/tasks/abc187_b）
```
n = gets.to_i
xy = n.times.map { gets.split.map(&:to_i) }
cnt = 0
xy.combination(2).each { |i|
  t = (i[1][1] - i[0][1]).to_f / (i[1][0] - i[0][0])
  cnt += 1 if -1.0 <= t && t <= 1.0
}
puts cnt

# 別解
n = gets.to_i
# x軸、y軸それぞれ全ての数を格納した配列を作成
x, y = n.times.map { gets.split.map(&:to_i)}.transpose
# x軸(x.combination(2))、y軸(y.combination(2))それぞれ全ての組み合わせを出力
# (0..n-1).to_a = [*0..n-1]
puts [*0..n-1].combination(2).select { |i, j| (y[j] - y[i]).abs <= (x[j] - x[i]).abs}.count

# 別解
n = gets.to_i
xy = n.times.map { gets.split.map(&:to_i) }
# 2点(x1, y1),(x2, y2)を通る直線の傾きは y1-y2 / x1-x2
puts xy.combination(2).count { |(x1, y1), (x2, y2)| (y1 - y2).abs <= (x1 - x2).abs }
```

- C問題（https://atcoder.jp/contests/abc187/tasks/abc187_c）
```
n = gets.to_i
s = n.times.map{gets.chomp}
s.uniq!

ans = s.group_by { |s| s.delete("!") }.select { |k, v| v.size > 1 }
puts ans.empty? ? "satisfiable" : ans.first[0]
```
