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

- C問題
```
# n個の区間のうち最も長い物を通らず、それ以外の区間をちょうど1度だけ通れば良い
k, n = gets.split.map(&:to_i)
a = gets.split.map(&:to_i)
cnt = a.each_cons(2).map { |a, b| b - a }
cnt << k + a.first - a.last
ans = k - cnt.max
puts ans
```
