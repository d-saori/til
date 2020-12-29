- A問題（https://atcoder.jp/contests/abc154/tasks/abc154_a）

```
s, t = gets.chomp.split.map(&:to_s)
a, b = gets.chomp.split.map(&:to_i)
u = gets.chomp.to_s

if s == u
  puts "#{a - 1} #{b}"
  # puts [a - 1, b].join(' ')
else t == u
  puts "#{a} #{b - 1}"
  # puts [a, b - 1].join(' ')
end 
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
