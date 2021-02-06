- A問題（https://atcoder.jp/contests/abc160/tasks/abc160_a）

```
s = gets
puts s[2] == s[3] && s[4] == s[5] ? "Yes" : "No"
```

- B問題
```
x = gets.to_i
goo = x / 500
g = (x - 500 * goo) / 5
puts goo * 1000 + g * 5

# 別解
x = gets.to_i
puts x / 500 * 1000 + x / 5 * 5
```
