- A問題（https://atcoder.jp/contests/abc116/tasks/abc116_a）

```
ab, bc, ca = gets.split.map(&:to_i)
puts ab * bc / 2
```

- B問題
```
s = gets.to_i
# 初めて同じ数が出てくるのは何番目か求める
t = []
loop do
  break if t.include?(s)
  t << s
  s.odd? ? s = 3 * s + 1 : s = s / 2
end
puts t.size + 1

# 別解
s = gets.to_i
# 初めて同じ数が出てくるのは何番目か求める
t = [s]
while
  s = s.odd? ? 3 * s + 1 : s / 2
  break if t.include?(s)
  t << s
end
puts t.size + 1
``｀

- C問題
```
n = gets.to_i
h = gets.split.map(&:to_i)
ans = 0
(1..h.size-1).each { |i|
  if h[i-1] > h[i]
    ans += h[i-1] - h[i]
  end
}
ans += h[-1]
puts ans
```
