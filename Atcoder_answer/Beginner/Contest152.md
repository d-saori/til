- A問題（https://atcoder.jp/contests/abc152/tasks/abc152_a）

```
n, m = gets.split.map(&:to_i)
puts n == m ? "Yes" : "No"
```

- B問題
```
a, b = gets.split.map(&:to_i)
a_ary = []
b_ary = []
b.times {
  a_ary << a
}
a.times {
  b_ary << b
}
puts [a_ary.join, b_ary.join].min

# 別解
a, b = gets.split.map(&:to_i)
puts [a.to_s * b, b.to_s * a].min
```
