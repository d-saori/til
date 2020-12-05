- A問題（https://atcoder.jp/contests/arc110/tasks/arc110_a）
```
# 自分の解答：最小公倍数に+1の数を求めた（入力例1のみクリア）
n = gets.to_i
puts 2.lcm(n) + 1

# 正解例
n = gets.to_i
puts (2..n).map.inject { |a, b| a.lcm(b) } + 1

n = gets.to_i
ans = 2
(2..n).each { |i|
  ans = ans.lcm(i)
}
puts ans + 1
```
