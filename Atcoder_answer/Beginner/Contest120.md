- A問題（https://atcoder.jp/contests/abc120）

```
a, b, c = gets.split.map(&:to_i)
puts a * c < b ? c : b / a

# 別解
a, b, c = gets.split.map(&:to_i)
puts [b / a, c].min
```

- B問題（https://atcoder.jp/contests/abc120/tasks/abc120_b）
```
a, b, k = gets.split.map(&:to_i)
ary = []
(1..[a, b].min).each { |i|
  ary << i if a & i == 0 && b % i == 0
}
puts ary[-k]

# 別解
a, b, k = gets.split.map(&:to_i)
puts a.gcd(b).downto(1).select {|i| a % i == 0 && b % i == 0 }[k - 1]

# 別解
a, b, k = gets.split.map(&:to_i)
min = [a, b].min
num = (1..min).select { |i| a % i == 0 && b % i == 0 }.sort.reverse
puts num[k-1]
```

- C問題
```
s = gets.chomp.chars
# 文字列sに0も1も1つ以上残っている場合、どこかで0と1が隣り合っている
# 0と1の個数を数え、それぞれc0,c1とすると、どのような順番で取り除いてもmin(c0,c1)回取り除く操作ができる
s0 = s.count("0")
s1 = s.count("1")
puts s0 >= 1 && s1 >= 1 ? 2 * [s0, s1].min : 0

# 別解
s = gets.chomp
# 文字列sに0も1も1つ以上残っている場合、どこかで0と1が隣り合っている
# 文字列sに含まれる0と1の個数をそれぞれ数え、c0とc1する
# どのような順番で取り除いてもmin(c0, c1)回取り除く操作ができる
# 取り除けるキューブの個数の最大値 = 2 * min(c0, c1)
cnt0 = s.count("0")
cnt1 = s.count("1")
puts [cnt0, cnt1].min * 2
```
