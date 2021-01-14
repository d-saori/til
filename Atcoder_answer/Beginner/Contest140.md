- A問題（https://atcoder.jp/contests/abc140/tasks/abc140_a）

```
n = gets.to_i
puts n ** 3
```

- B問題
```
n = gets.to_i
a = gets.split.map(&:to_i)
b = gets.split.map(&:to_i)
c = gets.split.map(&:to_i)
ans = b.sum
n.times { |i|
  ans += c[a[i] - 1] if a[i] + 1 == a[i + 1]
}
puts ans
```
