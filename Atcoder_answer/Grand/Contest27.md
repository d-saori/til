- A問題（https://atcoder.jp/contests/agc027/tasks/agc027_a）
```
n, x = gets.split.map(&:to_i)
a = gets.split.map(&:to_i).sort
ans = 0

a.each { |i|
  break if i > x
  x -= i # x = x - i
  ans += 1
}
ans -= 1 if ans == n && x > 0
puts ans
```
