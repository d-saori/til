- A問題（https://atcoder.jp/contests/arc105/tasks/arc105_a）
```
a, b, c, d = gets.split.map(&:to_i).sort
# sort順の場合食べるクッキーと残るクッキーの美味しさの総和が等しくなる条件は以下の2つ
# a + d = b + c
# a + b + c = d
puts a + d == b + c || a + b + c == d ? "Yes" : "No"
```
