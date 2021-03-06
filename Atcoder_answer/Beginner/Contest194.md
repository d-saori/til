- A問題
```
a, b = gets.split.map(&:to_i)
if a + b >= 15 && b >= 8
  puts 1
elsif a + b >= 10 && b >= 3
  puts 2
elsif a + b >= 3
  puts 3
else
  puts 4
end
```

- B問題
```
n = gets.to_i
a, b = n.times.map { gets.split.map(&:to_i) }.transpose
am = a.sort
bm = b.sort
sum = [am[0], bm[0]].max
if a.index(am[0]) == b.index(bm[0])
  ss = [am[1], bm[0]].max
  si = [am[0], bm[1]].max
  sum = [am[0] + bm[0], ss, si].min
end
puts sum
```

- C問題
```
n = gets.to_i
a = gets.split.map(&:to_i)
aa = a.map { |i| i ** 2 }
b = aa.sum
c = a.sum
puts n * b - c ** 2
```
