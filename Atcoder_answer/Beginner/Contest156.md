- A問題（https://atcoder.jp/contests/abc156/tasks/abc156_a）

```
n, r = gets.split(" ").map(&:to_i)

if n >= 10
  puts r
else
  puts r + 100 * (10 - n)
end
```
