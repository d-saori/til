- A問題（https://atcoder.jp/contests/abc112/tasks/abc112_a）

```
n = gets.to_i

if n == 1
  puts "Hello World"
else n == 2
  a = gets.to_i
  b = gets.to_i
  puts a + b
end
```

- B問題
```
n, t = gets.split.map(&:to_i)
s = []
n.times {
  c, ta = gets.split.map(&:to_i)
  s << c if ta <= t
}
puts s.empty? ? "TLE" : s.min

# 別解
n, t = gets.split.map(&:to_i)
a = n.times.map { gets.split.map(&:to_i) }.select { |c, ta| ta <= t}
puts a.empty? ? "TLE" : a.min[0]
```
