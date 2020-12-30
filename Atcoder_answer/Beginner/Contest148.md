- A問題（https://atcoder.jp/contests/abc148/tasks/abc148_a）

```
a = gets.to_i
b = gets.to_i

all = [1, 2, 3]
all.delete(a)
all.delete(b)
puts all
```

- B問題（https://atcoder.jp/contests/abc148/tasks/abc148_b）
```
n = gets.to_i
s, t = gets.split
puts s.chars.zip(t.chars).join

もしくは
n = gets.to_i
s, t = gets.split
ans = ""
n.times { |i|
  ans += s[i] + t[i]
}
puts ans
```

- C問題（https://atcoder.jp/contests/abc148/tasks/abc148_c）
```
a, b = gets.split.map(&:to_i)
puts a.lcm(b)
```
