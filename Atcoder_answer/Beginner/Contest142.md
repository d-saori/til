- A問題（https://atcoder.jp/contests/abc142/tasks/abc142_a）

```
n = gets.to_f
puts (n / 2.0).ceil / n

# 別解
n = gets.to_i
if n.odd?
  p (n / 2 + 1) / n.to_f
else 
  p (n / 2) / n.to_f
end

# 別解
n = gets.to_i
odd = []
[*1..n].each { |i|
  if i % 2 != 0
    odd << i
  end
}
puts odd.size / n.to_f
```
