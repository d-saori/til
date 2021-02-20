- A問題（https://atcoder.jp/contests/abc117/tasks/abc117_a）

```
t, x = gets.split.map(&:to_f)
puts t / x
```

- B問題
```
n = gets.to_i
l = gets.split.map(&:to_i).sort.reverse
puts l[0] < l[1..-1].sum ? "Yes" : "No"
```
