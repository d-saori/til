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
