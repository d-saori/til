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
```
