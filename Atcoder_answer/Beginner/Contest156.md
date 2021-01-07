- A問題（https://atcoder.jp/contests/abc156/tasks/abc156_a）

```
n, r = gets.split.map(&:to_i)
puts n >= 10 ? r : 100 * (10 - n) + r
```

- B問題（https://atcoder.jp/contests/abc156/tasks/abc156_b）
```
n, k = gets.split.map(&:to_i)
# N を K で割ったときの商で置き換える、という操作を N が 0 になるまで行うと、操作を行った回数が N を K 進数で表したときの桁数になる
ans = 0
while n > 0
  n = n / k
  ans += 1
end
puts ans

もしくは
n, k = gets.split.map(&:to_i)
puts n.to_s(k).size
```
