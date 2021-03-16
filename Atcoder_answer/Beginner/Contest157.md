- A問題（https://atcoder.jp/contests/abc157/tasks/abc157_a）

```
n = gets.chomp.to_i
puts (n / 2.to_f).ceil

もしくは
n = gets.to_f
puts (n / 2).round
```

- B問題
```
a = 3.times.map { gets.split.map(&:to_i) }.flatten
ans = []
n = gets.to_i
n.times {
  b = gets.to_i
  idx = a.find_index(b)
  s << idx
  # idxがnilではない時
  ans << idx if idx != nil #=> # ans[idx] = true if idx
}
# ◯が並んでるかを判定(縦3通り、横3通り、斜め2通り)
# 縦:[0, 3, 6], [1, 4, 7], [2, 5, 8]
# 横:[0, 1, 2], [3, 4, 5], [6, 7, 8]
# 斜め:[0, 4, 8], [2, 4, 6]
# any?:全ての要素が真だとtrueを返す
puts [[0, 3, 6], [1, 4, 7], [2, 5, 8], [0, 1, 2], [3, 4, 5], [6, 7, 8], [0, 4, 8], [2, 4, 6]].any? { |i| i.all? { |j| ans[j] }} ? "Yes" : "No"
```
