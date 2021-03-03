- A問題
```
a, b, c, d = gets.split.map(&:to_f)
if b / a > d / c
  puts "TAKAHASHI"
elsif b / a < d / c
  puts "AOKI"
else
  puts "DRAW"
end
```

- B問題
```
n, m = gets.split.map(&:to_i)
# 長針は1時間ごとに360/12=30度、1分ごとに360/12/60=0.5度動く
# 短針は1分ごとに360/60で6度動く
# 長針と短針が12時の方向から見てどれだけ進んでいるかを0〜360度の少数で表し、差を取る
# 180度より大きい時、大きい方の角を見てしまっているため、360度から差の角を引いたものが答え
hour = 30 * (n % 12) + m / 2
min = 6 * m
d = (hour - min).abs
puts d > 180 ? 360 - d : d
```
