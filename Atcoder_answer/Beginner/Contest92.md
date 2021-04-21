- A問題
```
a = gets.to_i
b = gets.to_i
c = gets.to_i
d = gets.to_i
ab = [a, b].min
cd = [c, d].min
puts ab + cd

# 短く
a, b, c, d = 4.times.map {gets.to_i}
puts [a, b].min + [c, d].min
```

- B問題
```
n = gets.to_i
d, x = gets.split.map(&:to_i)
# i人目の参加者は合宿中にチョコレートを1+[(d-1)/a]個食べる
n.times {
  a = gets.to_i
  x += (d + a - 1) / a
}
puts x

# 別解
n = gets.to_i
d, x = gets.split.map(&:to_i)
# i人目の参加者は合宿中にチョコレートを1+[(d-1)/a]個食べる
n.times {
  a = gets.to_i
  x += (d - 1) / a + 1
}
puts x

# 別解
n = gets.to_i
d, x = gets.split.map(&:to_i)
n.times {
  a = gets.to_i
  day = 1
  i = 1
  while true
    break if day > d
    x += 1
    day = i * a + 1
    i += 1
  end
}
puts x
```

- C問題
```
n = gets.to_i
a = gets.split.map(&:to_i)
a = a.unshift(0).push(0)
s = 0
(n + 1).times { |i|
  s += (a[i + 1] - a[i]).abs
}
n.times { |i|
  s_i = s + (a[i] - a[i + 2]).abs - (a[i] - a[i + 1]).abs - (a[i + 1] - a[i + 2]).abs
  puts s_i
}
```
