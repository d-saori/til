- A問題（https://atcoder.jp/contests/abc067/tasks/abc067_a）
```
a, b = gets.split.map(&:to_i)
if a % 3 == 0 || b % 3 == 0 || (a + b) % 3 == 0
  puts "Possible"
else
  puts "Impossible"
end
```

- B問題（https://atcoder.jp/contests/abc067/tasks/abc067_b）
```
n, k = gets.split.map(&:to_i)
l = gets.split.map(&:to_i).sort.reverse
puts l[0..k - 1].sum
```

- C問題
```
n = gets.to_i
a = gets.split.map(&:to_i)
y = a.sum
x = 0
ans = 10 ** 12
a.pop
a.each { |i|
  x += i
  y -= i
  z = (y - x).abs
  ans = z if ans > z
}
puts ans.abs
```
