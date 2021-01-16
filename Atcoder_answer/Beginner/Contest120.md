- A問題（https://atcoder.jp/contests/abc120）

```
a, b, c = gets.split.map(&:to_i)
puts a * c < b ? c : b / a

# 別解
a, b, c = gets.split.map(&:to_i)
puts [b / a, c].min
```

- B問題（https://atcoder.jp/contests/abc120/tasks/abc120_b）
```
a, b, k = gets.split.map(&:to_i)
ary = []
(1..[a, b].min).each { |i|
  ary << i if a & i == 0 && b % i == 0
}
puts ary[-k]
```
