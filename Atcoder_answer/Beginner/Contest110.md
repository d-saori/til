- A問題（https://atcoder.jp/contests/abc110/tasks/abc110_a）

```
a, b, c = gets.split.map(&:to_i).sort.reverse
ab = "#{a}#{b}"
cc = "#{c}"
puts ab.to_i + cc.to_i

# 別解
# 1番大きい要素が10の桁 = *10
abc = gets.split.map(&:to_i).sort.reverse
puts abc[0] * 10 + abc[1] + abc[2]
```
