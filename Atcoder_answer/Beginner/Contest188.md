- A問題
```
x, y = gets.split.map(&:to_i)
puts (x - y).abs < 3 || (y - x).abs < 3 ? "Yes" : "No"
```

- B問題
```
n = gets.to_i
a = gets.split.map(&:to_i)
b = gets.split.map(&:to_i)
puts a.zip(b).map { |x, y| x * y}.sum == 0 ? "Yes" : "No"
```

- C問題
```
n = gets.to_i
a = gets.split.map(&:to_i)
# 準優勝するのは、優勝する( = 一番レートが高い) 選手とは逆側のブロックにいる選手のうち一番レートが高い人
# 2ブロックに分ける
s = a.size / 2
# a[start, length]
x = a[0, s]
y = a[s, s]
mx = x.max
my = y.max
sf = [mx, my].min
puts a.index(sf) + 1

# 別解
n = gets.to_i
a = gets.split.map(&:to_i)
one = a[0..a.size/2 - 1]
two = a[a.size/2..-1]
s = [one.max, two.max].min
puts a.index(s) + 1
```
