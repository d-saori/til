- A問題（https://atcoder.jp/contests/abc126/tasks/abc126_a）

```
n, k = gets.split.map(&:to_i)
s = gets
s[k - 1] = s[k - 1].downcase
puts s

# 別解
n, k = gets.split.map(&:to_i)
s = gets.chomp.chars
s[k-1].downcase!
puts s.join
```

- B問題
```

```
