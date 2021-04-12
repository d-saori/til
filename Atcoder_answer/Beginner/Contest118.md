- A問題（https://atcoder.jp/contests/abc118/tasks/abc118_a）

```
a, b = gets.split.map(&:to_i)
if b % a == 0
  puts a + b
else
  puts b - a
end
```

- B問題
```
n, m = gets.split.map(&:to_i)
cnt = 0
s = []
t = []
n.times {
  a = gets.split.map(&:to_i)
  s << a
}
s.each { |i|
  t << i.drop(1)
}
b = t.flatten.group_by(&:itself).values.map(&:size)
b.each { |j|
  cnt += 1 if j == n
}
puts cnt

# 別解
n, m = gets.split.map(&:to_i)
ary = []
n.times {
  ary += gets.split.map(&:to_i)[1..-1]
}
puts (1..m).map { |i| ary.count(i) }.count(n)
```

- C問題
```
# 入力例1の場合、どのモンスターも初期体力が偶数なので、攻撃してたいちょくが変化しても偶数にしか変化しない
# aもb(b>a)もxの倍数なら、b-aもxの倍数
# 最大公約数gとすると、常にxとしてgを取れるので生きているモンスターの体力は必ずgの倍数となる
n = gets.to_i
a = gets.split.map(&:to_i)
g = a[0]
a.each { |i|
  g = g.gcd(i)
}
puts g
```
