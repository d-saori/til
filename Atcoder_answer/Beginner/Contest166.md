- A問題（https://atcoder.jp/contests/abc166/tasks/abc166_a）

```
s = gets.chomp
puts s == "ABC" ? "ARC" : "ABC"
```

- B問題
```
n, k = gets.split.map(&:to_i)
d = []
a = []
k.times {
  d << gets.to_i
  a << gets.split.map(&:to_i)
}
puts n - a.flatten.uniq.size
```
