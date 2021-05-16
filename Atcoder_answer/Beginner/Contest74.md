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

# 別解
n = gets.to_i
k = gets.to_i
x = gets.split.map(&:to_i)
total = 0
x.each { |i|
  total += [(i - 0).abs * 2, (i - k).abs * 2].min
}
puts total
```
