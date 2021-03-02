- A問題
```
s = gets.chomp
puts s[-1] == "T" ? "YES" : "NO"
```

- B問題
```
hw = 2.times.map { gets.split.map(&:to_i) }
puts hw[0][0] == hw[1][0] || hw[0][0] == hw[1][1] || hw[0][1] == hw[1][0] || hw[0][1] == hw[1][1] ? "YES" : "NO"

# 別解
h, w = 2.times.map { gets.chomp.split }
puts (h.include?(w[0]) || h.include?(w[1])) ? "YES" : "NO"
```
