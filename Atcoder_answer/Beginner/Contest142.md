- A問題（https://atcoder.jp/contests/abc142/tasks/abc142_a）

```
n = gets.to_f
puts (n / 2.0).ceil / n

もしくは

n = gets.to_i
if n.odd?
  p (n / 2 + 1) / n.to_f
else 
  p (n / 2) / n.to_f
end
```
