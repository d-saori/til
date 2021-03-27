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
