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

- B問題
```
n, m, x, y = gets.split.map(&:to_i)
xa = gets.split.map(&:to_i)
ya = gets.split.map(&:to_i)
z = [*x..y]
cnt = 0
z.each { |i|
  cnt += 1 if x < i && i <= y && i > xa.max && i <= ya.min
}
puts cnt >= 1 ? "No War" : "War"
```
