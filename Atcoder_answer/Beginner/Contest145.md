- A問題（https://atcoder.jp/contests/abc145/tasks/abc145_a）

```
r = gets.to_i
puts r ** 2

# 1行で
puts gets.to_i ** 2
```

- B問題
```
n = gets.to_i
s = gets.chomp
c = n / 2
s_f = s[0..c-1]
s_e = s[c..-1]
puts n.even? && s_f == s_e ? "Yes" : "No"

# 別解
n = gets.to_i
s = gets.chomp
t = s[0, n / 2] * 2
puts s == t ? "Yes" : "No"
```
