- A問題（https://atcoder.jp/contests/abc153/tasks/abc153_a）

```
h, a = gets.chomp.split.map(&:to_i)
puts (h / a.to_f).ceil

# 別解
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

# 別解
h, a = gets.split.map(&:to_i)
puts h % a == 0 ? h / a : h / a + 1
```

- B問題
```

```
