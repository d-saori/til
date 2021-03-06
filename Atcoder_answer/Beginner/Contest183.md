- A問題（https://atcoder.jp/contests/abc183/tasks/abc183_a）

```
x = gets.to_i
if x >= 0
  puts x
else
  puts 0
end
```

- B問題（https://atcoder.jp/contests/abc183/tasks/abc183_b）

```
sx, sy, gx, gy = gets.split.map(&:to_i)
# x軸で跳ね返る=現在地点と目標地点を結ぶ直線とx軸の交点を求める
# y軸の変化量より現在地点から目標地点までを sy : gy に内分する点でx軸と交わる
# sxからgxへの変化をsy:gyに内分する座標を求める
puts ((sx * gy) + (gx * sy)) / (sy + gy).to_f

# 別解
sx, sy, gx, gy = gets.split.map(&:to_f)
puts sx + sy * (gx - sx) / (sy - gy)
```

- C問題
```
n, k = gets.split.map(&:to_i)
t = n.times.map { gets.split.map(&:to_i) }
cnt = 0
# 都市1から移動するので1は固定で2から開始
[*2..n].permutation { |i|
  i.unshift(1)
  i << 1
  sum = 0
  n.times { |j|
    sum += t[i[j] - 1][i[j + 1] - 1]
  }
  cnt += 1 if sum == k
}
puts cnt

# 別解
n, k = gets.split.map(&:to_i)
t = n.times.map { gets.split.map(&:to_i) }
cnt = 0
[*2..n].permutation { |i|
  i.unshift(1)
  i << 1
  road = i.each_cons(2).map { |a, b| t[a - 1][b - 1] }.sum
  cnt += 1 if road == k
}
puts cnt
```
