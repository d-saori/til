- A問題（https://atcoder.jp/contests/abc155/tasks/abc155_a）

```
ary = gets.split.map(&:to_i)
puts ary.uniq.size == 2 ? "Yes" : "No"
```

- B問題
```
n = gets.to_i
a = gets.split.map(&:to_i)
even = a.select { |i| i.even? }
cnt = 0
even.each { |j|
  cnt += 1 if j % 3 == 0 || j % 5 == 0
}
puts cnt == even.size ? "APPROVED" : "DENIED"

# 別解
n = gets.to_i
a = gets.split.map(&:to_i)
puts a.select(&:even?).all? { |i| i % 3 == 0 || i % 5 == 0 } ? "APPROVED" : "DENIED"
```
