- A問題（https://atcoder.jp/contests/abc164/tasks/abc164_a）

```
s, w = gets.split.map(&:to_i)
puts s <= w ? "unsafe" : "safe"
```

- B問題
```
a, b, c, d = gets.split.map(&:to_i)
# 高橋君のモンスターの体力が0以下になるのは青木君の[a / d]回目の攻撃
# 青木君のモンスターの体力が0以下になるのは高橋君の[b / c]回目の攻撃
# [a / d] >= [b / c] なら高橋君の勝ち
puts a / d >= b / c ? "Yes" : "No"

# 別解答
a, b, c, d = gets.split.map(&:to_i)
while true do
  c -= b
  break if c <= 0
  a -= d
  break if a <= 0
end
puts a > 0 ? "Yes" : "No"
```
