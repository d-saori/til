- A問題
```
n = gets.chomp.chars
puts n.uniq.size == 1 ? "SAME" : "DIFFERENT"
```

- B問題
```
n = gets.to_i
y = []
z = []
n.times {
  s, p = gets.chomp.split
  y << s
  z << p.to_i
}
s_z = z.sum / 2
ans = []
(0..n-1).each { |i|
  if z[i] > s_z
    ans << y[i]
  else
    ans << "atcoder"
  end
}
ans.delete_if { |j|
  j == "atcoder"
}
puts ans.size == 0 ? "atcoder" : ans

# 別解
n = gets.to_i
sp = n.times.map { gets.chomp.split }
u = sp.map { |s, p| p.to_i }.sum
t = sp.find { |s, p| 2 * p.to_i > u }
puts t ? t[0] : "atcoder"
```
