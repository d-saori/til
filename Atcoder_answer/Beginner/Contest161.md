- A問題(https://atcoder.jp/contests/abc161/tasks/abc161_a)

```
x, y, z = gets.split.map(&:to_i)
puts "#{z} #{x} #{y}"

# 別解答例
x, y, z = gets.split(" ").map(&:to_i)
puts [z, x, y].join(" ")
```

- B問題
```
n, m = gets.split.map(&:to_i)
a = gets.split.map(&:to_i).sort.reverse
s = a.sum / (4 * m).to_f
cnt = 0
a[0..m-1].each { |i|
  cnt += 1 if i >= s
}
puts cnt >= m ? "Yes" : "No"

# 別解
n, m = gets.split.map(&:to_i)
a = gets.split.map(&:to_i).sort.reverse
poll = a.sum
puts m <= a.count { |i| i >= poll / (4.0 * m) } ? "Yes" : "No"

# 別解
n, m = gets.split.map(&:to_i)
a = gets.split.map(&:to_i).sort.reverse
poll = a.sum / (4.0 * m)
puts a[m - 1] >= poll ? "Yes" : "No"
```

- C問題
```
n, k = gets.split.map(&:to_i)
# xがk以上の時、操作を行うことでx-kとなる
# nからn/k回操作を行うことで、整数はnをkで割った余りとなる
# nをkで割った余りをtとし、tに操作を行うとk-tとなる
# k-tに操作を行うとtに戻るだけなので、k以下の値として取りうるものはtとk-tの小さい方
puts [n % k, (k - n % k).abs].min
```
