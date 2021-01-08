- A問題（https://atcoder.jp/contests/abc153/tasks/abc153_a）

```
h, a = gets.chomp.split.map(&:to_i)
puts (h / a.to_f).ceil

# 別解答
h, a = gets.split.map(&:to_i)
ans = 0
while true
  h -= a
  ans += 1
  if h <= 0
    puts ans
    break
  end
end
```
