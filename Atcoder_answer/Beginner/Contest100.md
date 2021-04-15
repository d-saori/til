- A問題（https://atcoder.jp/contests/abc100/tasks/abc100_a）

```
a, b = gets.split.map(&:to_i)
if a > 8 || b > 8
  puts ":("
else
  puts "Yay!"
end
```

- B問題（https://atcoder.jp/contests/abc100/tasks/abc100_b）

```
d, n = gets.split.map(&:to_i)

n = 101 if n == 100

if d == 0
  puts n
elsif d == 1
  puts n * 100
else 
  puts n * 10000
end
```

- C問題
```
n = gets.to_i
a = gets.split.map(&:to_i)
cnt = 0
a.each { |i|
  while i.even?
    i /= 2
    cnt += 1
  end
}
puts cnt
```
