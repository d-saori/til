- A問題
```
a, b = gets.split.map(&:to_i)
puts a * b % 2 == 0 ? "Even" : "Odd"
```

- B問題
```
a, b = gets.chomp.split
n = (a + b).to_i
m = (n ** (1 / 2.0)).floor
puts m ** 2 == n ? "Yes" : "No"

# 別解
a, b = gets.chomp.split
n = (a + b).to_i
m = Math.sqrt(n).to_i
puts m ** 2 == n ? "Yes" : "No"

# 別解
a, b = gets.chomp.split
c = (a + b).to_f
puts (c ** 0.5).ceil == c ** 0.5 ? "Yes" : "No"
```

- C問題
```
n = gets.to_i
pt = 0
px = 0
py = 0
n.times {
  t, x, y = gets.split.map(&:to_i)
  diff = (px - x).abs + (py - y).abs
  dt = t - pt
  if diff > dt || (diff - dt) % 2 == 1
    puts "No"
    return
  end
  pt = t
  px = x
  py = y
}
puts "Yes"
```
