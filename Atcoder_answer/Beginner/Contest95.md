- A問題（https://atcoder.jp/contests/abc095/tasks/abc095_a）
```
s = gets.chomp.split("")
a = s.count("o")
puts 700 + 100 * a

もしくは
s = gets.chomp
puts 700 + (s.count("o") * 100)　など
```

- B問題（https://atcoder.jp/contests/abc095/tasks/abc095_b）
```
n, x = gets.split.map(&:to_i)
a = []
n.times {
  m = gets.to_i
  a << m
}
min = a.min
b = x - a.sum
puts b == 0 ? n : b / min + n

# 別解
n, x = gets.split.map(&:to_i)
a = n.times.map{gets.to_i}

# この3行省略できる
# b = x - a.sum # 残りのお菓子の素量
# min = a.min # 素の消費量が一番少ない
# puts n + (b / min)

puts n + (x - a.sum) / (a.min)
```

- c問題（https://atcoder.jp/contests/abc095/tasks/arc096_a）
```
a, b, c, x, y = gets.split.map(&:to_i)
ma = a * x
mb = b * y
mc = 2 * c * [x, y].max
md = 2 * c * [x, y].min
if x > y
  md += a * (x - y)
else
  md += b * (y - x)
end
puts [ma + mb, mc, md].min

もしくは
a, b, c, x, y = gets.split.map(&:to_i)
z = [x, y].min
puts [
  a * x + b * y,
  a * (x - z) + b * (y - z) + 2 * c * z,
  2 * c * [x, y].max
].min

a, b, c, x, y = gets.split.map(&:to_i)
z = (a * x) + (b * y)
min = [x, y].min
max = [x, y].max
w = max * 2 * c
s = min * 2 * c
if x > y
  t = (x - y) * a
else
  t = (y - x) * b
end
puts [z, s + t, w].min
```
