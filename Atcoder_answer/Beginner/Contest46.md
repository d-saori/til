- A問題
```
abc = gets.split.map(&:to_i)
puts abc.uniq.size
```

- B問題
```
n, k = gets.split.map(&:to_i)
# 左端のボールに塗る色をを決める:k通り
# 左から順番に塗る色を決める。左に塗られている色以外から:k-1通り
# 全体では k * (k - 1)通り
ans = k
(n - 1).times {
  ans *= (k - 1)
}
puts ans

# 別解
n, k = gets.split.map(&:to_i)
puts k * (k - 1) ** (n - 1)
```
