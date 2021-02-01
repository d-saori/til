- A問題（https://atcoder.jp/contests/abc182/tasks/abc182_a）

```
a, b = gets.split.map(&:to_i)

puts (2 * a + 100) - b
```

<br>

- B問題（https://atcoder.jp/contests/abc182/tasks/abc182_b）
```
n = gets.to_i
a = gets.split.map(&:to_i)
k = []
# k >= 1000だとGCD度は0なので、2 <= k <= 1000の範囲を全探索する
(2..1000).each { |i|
  cnt = 0
  a.each { |j|
    cnt += 1 if j % i == 0
  }
  k << cnt
}
puts (k.index(k.max) + 2)


# 別解
n = gets.to_i
a = gets.split.map(&:to_i)
puts (2..1000).max_by { |k| a.count { |a| a % k == 0 }}
```
