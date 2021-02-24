- A問題（https://atcoder.jp/contests/abc085/tasks/abc085_a）
```
s = gets
puts s.gsub(/2017/, "2018")
```

- B問題
```
n = gets.to_i
d = n.times.map { gets.to_i }.sort
puts d.uniq.size
```
