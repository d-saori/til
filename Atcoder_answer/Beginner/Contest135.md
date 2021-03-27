- A問題（https://atcoder.jp/contests/abc135/tasks/abc135_a）

```
a, b = gets.split.map(&:to_i)
puts (a + b) % 2 == 0 ? (a + b) / 2 : "IMPOSSIBLE"
```

- B問題
```
n = gets.to_i
p = gets.split.map(&:to_i)
a = [*1..n].reverse
if p == [*1..n]
  puts "YES"
else
  b = p.count { |i| i != a.pop }
  puts b == 2 ? "YES" : "NO"
end

# 別解
n = gets.to_i
p = gets.split.map(&:to_i)
# pとpが昇順時と異なる数をkとした場合、k<=2である時に限り1回以下のスワップでpを昇順にする事が可能。k=0の時は元から昇順
cnt = 0
n.times { |i|
  cnt += 1 if p[i] != i + 1
}
puts cnt <= 2 ? "Yes" : "No"
```

- C問題
```
b = gets.split.map(&:to_i)
# 1番目の街は1番目の勇者に救ってもらうしかない
# 1番目の勇者は1番目の街のモンスターを全力でmin(a1, b1)体倒し、残った力で2番目の街のモンスターを全力でmin(a2b1-min(a1b1))体倒すのが最適
t = 0
n.times { |i|
  m = [a[i], b[i]].min
  t += m
  a[i] -= m
  b[i] -= m
  m = [a[i+1], b[i]].min
  t += m
  a[i+1] -= m
  b[i] -= m
}
puts t

# 別解
b = gets.split.map(&:to_i)
ans = 0
n.times { |i|
  m = [a[i], b[i]].min
  ans += m
  m = [a[i+1], b[i] - m].min
  ans += m
  a[i+1] -= m
}
puts ans
```
