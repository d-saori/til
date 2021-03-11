- A問題(https://atcoder.jp/contests/abc177/tasks/abc177_a)

```
# 自分の回答
D, T, S = gets.split.map(&:to_i)

if T > D / S
  puts "Yes"
else
  puts "No"
end
```

<br>

- 高橋くんが何分で到着出来るかを求めてしまえば、あとは比較をするだけで解くことが出来る。
  - 到着するまでの時間は整数にはならない。
  - 多くのプログラミング言語では、整数同士で割り算を行うと、小数部分が切り捨てられ、整数となるので、小数として計算する。
  
```
d, t, s = gets.split.map(&:to_f)
puts d / s <= t ? "Yes" : "No"
```

- B問題
```
s = gets.chomp
t = gets.chomp
min = t.size
(0..s.size - t.size).each { |i|
  cnt = 0
  t.size.times { |j|
    cnt += 1 if s[i + j] != t[j]
  }
  min = cnt if cnt < min
}
puts min

# 別解
s = gets.chomp.chars
t = gets.chomp.chars
puts (0..s.size - t.size).map { |i|
  (0..t.size - 1).count { |j| t[j] != s[i + j] }
}.min

# 別解
ss, t = 2.times.map { gets.chomp.chars }
min = s.size
s.each_cons(t.size) { |i|
  cnt = 0
  i.each_with_index { |j, id|
    cnt += 1 if j != t[id]
  }
  min = [min, cnt].min
}
puts min
```
