- A問題（https://atcoder.jp/contests/abc134/tasks/abc134_a）

```
r = gets.to_i
puts 3 * (r ** 2)
```

- B問題
```
n, d = gets.split.map(&:to_i)
# 監視員1人は、2D+1の木を監視できる
# 2D+1=WとしたらN本の木を監視する人数はN/W
w = 2 * d + 1
puts (n / w.to_f).ceil
```
