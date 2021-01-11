- A問題
```
n, a, b = gets.split.map(&:to_i)
puts [n * a, b].min
```

- B問題
```
n = gets.chomp.to_i
a = n.to_s.split("").map { |i| i.to_i}.inject(:+)
# a = n.to_s.chars.map { |i| i.to_i}.inject(:+)
# a = n.to_s.split("").map { |i| i.to_i}.sum なども書き方もある
puts n % a == 0 ? "Yes" : "No"
```
