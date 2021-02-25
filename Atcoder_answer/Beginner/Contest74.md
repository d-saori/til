- A問題
```
n, a = 2.times.map { gets.to_i }
puts n * n - a
```

- B問題
```
n, k = 2.times.map { gets.to_i }
x = gets.split.map(&:to_i)
# タイプAのロボットで回収される時の移動距離:sx
# タイプBのロボットで回収される時の移動距離:2(k-x)
puts x.map { |i| [i - 0, k - i].min * 2 }.sum
```
