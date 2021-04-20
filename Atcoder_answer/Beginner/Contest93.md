- A問題（https://atcoder.jp/contests/abc093/tasks/abc093_a）
```
s = gets.chomp.chars.sort.join
puts s == "abc" ? "Yes" : "No"
```

- B問題（https://atcoder.jp/contests/abc093/tasks/abc093_b）
```
a, b, k = gets.split.map(&:to_i)
left = [*a...[a+k, b].min]
right = [*[b-k+1, a].max..b]
puts (left + right).uniq

# 別解
# b - a + 1 = aとbの間の整数の個数
# b - a + 1 > 2 * k
a, b, k = gets.split.map(&:to_i)
puts b - a + 1 > 2 * k ? [*a..a+k-1] + [*b-k+1..b] : [*a..b]
```

- C問題（https://atcoder.jp/contests/abc093/tasks/arc094_a）
```
a, b, c = gets.split.map(&:to_i)
# 数を増やして等しくするので最大値x([a, b, c].max)に合わせる
# どちらの操作をしても毎回増える全体の数は2 : 3x - (a + b + c) = 偶数
# 最終的(3つの数が等しくなった時)の合計 - 初期値の合計 / 2 = 操作した回数
# 3x と (a + b + c) の偶奇が等しくなった時の値はm、異なればm+1(2で割ると0.5部分はなくなるので+2)
ans = [a, b, c].max * 3 - (a + b + c)
puts ans.even? ? ans / 2 : (ans / 2) + 2
# puts ans.even? ? ans / 2 : (ans + 1) / 2 + 1
```
