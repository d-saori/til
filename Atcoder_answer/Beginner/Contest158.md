- A問題（https://atcoder.jp/contests/abc158/tasks/abc158_a）

```
s = gets.chomp
puts s == "AAA" || s == "BBB" ? "No" : "Yes"
```

- B問題
```
n, a, b = gets.split.map(&:to_i)
# 1回の操作をセットで考える
# n個のうち完全に含まれる操作の回数は、n/a+b回
# 中途半端に含まれる操作は高々1回分。nをa+bで割った余りとaの大小関係が重要
# nをa+bで割った余りをrとすると、min(r, a)だけ含まれる
puts n / (a + b) * a + [n % (a + b), a].min

# 別解
n, a, b = gets.split.map(&:to_i)
ans = (n / (a + b)) * a
t = n % (a + b)
if t >= a
  ans += a
else
  ans += t
end
puts ans
```
