- A問題（https://atcoder.jp/contests/abc107/tasks/abc107_a）

```
n, i = gets.split.map(&:to_i)

if n == 1
  puts i
else
  puts n - i + 1
end
```

- B問題
```
h, w = gets.split.map(&:to_i)
line = []
h.times {
  a = gets.chomp
  line << a if a.count("#") != 0
}
(w - 1).downto(0) { |i|
  if line.all? { |j| j[i] == "." }
    line.each { |j| j[i, 1] = "" }
  end
}
line.each { |j| puts j }
```
