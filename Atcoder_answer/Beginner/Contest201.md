- A問題
```
a, b, c = gets.split.map(&:to_i)
puts c - b == b - a || b - c == c - a || c - a == a - b || a - c == c - b || b - a == a - c || a - b == b - a ? "Yes" : "No" 

# 別解
a, b, c = gets.split.map(&:to_i).sort
puts c - b == b - a ? "Yes" : "No"
```

- B問題
```
n = gets.to_i
y = []
name = []
n.times {
  s, t = gets.chomp.split
  name << s
  y << t.to_i
}
yy = y.sort.reverse
z = yy[1]
z_name = y.index(z)
puts name[z_name]
```
