- A問題（https://atcoder.jp/contests/abc166/tasks/abc166_a）

```
s = gets.chomp
puts s == "ABC" ? "ARC" : "ABC"
```

- B問題
```
n, k = gets.split.map(&:to_i)
d = []
a = []
k.times {
  d << gets.to_i
  a << gets.split.map(&:to_i)
}
puts n - a.flatten.uniq.size
```

- C問題
```
n, m = gets.split.map(&:to_i)
h = gets.split.map(&:to_i)
ans = [] #=> 良くない展望台を入れる
m.times {
  a, b = gets.split.map(&:to_i)
  if h[a-1] == h[b-1]
    ans.push(a, b)
  elsif h[a-1] > h[b-1]
    ans << b
  else
    ans << a
  end
}
puts n - ans.uniq.size
```
