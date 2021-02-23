- A問題
```
# 猫の数は、B匹すべてが犬のときに最小 (A 匹) になり、B匹すべてが猫のときに最大 (A + B 匹) になる
a, b, x = gets.split.map(&:to_i)
puts a <= x && x <= a + b ? "YES" : "NO"

# 別解
a, b, x = gets.split.map(&:to_i)
puts a > x || a + b < x ? "NO" : "YES"
```

- B問題
```
n, m, x = gets.split.map(&:to_i)
a = gets.split.map(&:to_i)
# ゴールがマス0の時移動するマス数
# k0 = x - 0 => x
# ゴールがマスnの時移動するマス数
kn = 2 * n + 1 - x
cost0 = 0
costn = 0
(0..x).each { |i|
  cost0 += 1 if a.include?(i)  
}
(x..kn).each { |j|
  costn += 1 if a.include?(j)
}
puts [cost0, costn].min

# 別解
n, m, x = gets.split.map(&:to_i)
a = gets.split.map(&:to_i)
puts [a.count { |i| i < x }, a.count { |i| i > x }].min
```
