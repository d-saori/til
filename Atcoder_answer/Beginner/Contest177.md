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
