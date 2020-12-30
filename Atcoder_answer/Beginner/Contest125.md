- A問題（https://atcoder.jp/contests/abc125/tasks/abc125_a）

```
a, b, t = gets.split.map(&:to_i)

puts (t / a) * b
```

- B問題（https://atcoder.jp/contests/abc125/tasks/abc125_b）
```
n = gets.to_i
v = gets.split.map(&:to_i)
c = gets.split.map(&:to_i)

# x - y > 0 = 宝石を選ぶ(加算される)
ans = 0
v.zip(c).map{ |x, y| ans += x - y if x > y}
puts ans
```
