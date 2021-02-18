- A問題（https://atcoder.jp/contests/abc123/tasks/abc123_a）

```
a = gets.to_i
b = gets.to_i
c = gets.to_i
d = gets.to_i
e = gets.to_i
k = gets.to_i
# a,b,c,d,e,k = 6.times.map{gets.to_i} とも書ける

if e - a > k
  puts ":("
else 
  puts "Yay!"
end
```

- B問題
```
a = 5.times.map { gets.to_i }.sort_by { |i| (i - 1) % 10 }
puts a[0] + a[1..-1].map { |i| (i + 9) / 10 * 10 }.sum

# 別解
a = 5.times.map { gets.to_i }
b = a.map { |i| (i % 10) == 0 ? 0 : 10 - (i % 10) }
puts a.sum + b.sum - b.max
```
