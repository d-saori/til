- A問題
```
a, b = gets.split.map(&:to_i)
puts "#{b} #{a}"
```

- B問題
```
n = gets.to_i
h = (n / 3600.to_f).floor
m = (n - 3600 * h) / 60
s = n - (3600 * h) - (60 * m)
puts [h.to_s.rjust(2, "0"), m.to_s.rjust(2, "0"), s.to_s.rjust(2, "0a")].join(":")
```
