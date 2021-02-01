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
```
