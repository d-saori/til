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
```
