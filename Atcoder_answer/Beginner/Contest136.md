- A問題（https://atcoder.jp/contests/abc136/tasks/abc136_a）

```
a, b, c = gets.split.map(&:to_i)
puts b + c < a ? 0 : c - (a - b)

# 別解
a, b, c = gets.split.map(&:to_i)
puts [c - a + b, 0].max
```

- B問題（https://atcoder.jp/contests/abc136/tasks/abc136_b）
```
n = gets.to_i
sum = 0
[*1..n].each { |i|
  if i.to_s.size.odd?
  sum += 1
  end
}
puts sum
```
