- A問題（https://atcoder.jp/contests/abc061/tasks/abc061_a）
```
a, b, c = gets.split.map(&:to_i)
# if a <= c <= b
#   puts "Yes"
# else
#   puts "No"
# end
# 三項演算子
puts a <= c && c <= b ? "Yes" : "No"
```

- B問題（https://atcoder.jp/contests/abc061/tasks/abc061_b）
```
n, m = gets.split.map(&:to_i)
# 各都市から何本の道路が伸びているかを管理する配列
road = m.times.map{gets.split.map(&:to_i)}

# i番目の都市に注目し、各都市から他の都市に何本の道路が伸びているかを調べる
# (1..n).eachでもOK
1.upto(n) { |i|
  cnt = 0
# 全ての道路の両端にi番目の都市が含まれているか判定し、数える
  road.each { |r|
    cnt += 1 if r.include?(i)  # cnt = cnt + 1 if r.include?(i)
  }
# 数えた道路の本数をi番目の都市から伸びている道路の本数として出力
  puts cnt
}
```
