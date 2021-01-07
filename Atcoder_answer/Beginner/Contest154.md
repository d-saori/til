- A問題（https://atcoder.jp/contests/abc154/tasks/abc154_a）

```
s, t = gets.chomp.split
a, b = gets.chomp.split.map(&:to_i)
u = gets.chomp
puts u == s ? "#{a - 1} #{b}" : "#{a} #{b - 1}"
# puts u == s ? [a - 1, b].join(" ") : [a, b - 1].join(" ")
```

- B問題（https://atcoder.jp/contests/abc154/tasks/abc154_b）
```
s = gets
puts s.gsub(/[a-z]/, "x")
```

- C問題（https://atcoder.jp/contests/abc154/tasks/abc154_c）
```
n = gets.to_i
ary = gets.split.map(&:to_i)
puts ary.uniq.size == n ? "Yes" : "No"
```
