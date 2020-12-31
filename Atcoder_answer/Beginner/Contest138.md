- A問題（https://atcoder.jp/contests/abc138/tasks/abc138_a）
```
a = gets.to_i
s = gets.to_s

if a >= 3200
  puts s
else
  puts "red"
end
```

- B問題（https://atcoder.jp/contests/abc138/tasks/abc138_b）
```
n = gets.to_i
a = gets.split.map(&:to_i)
b = a.inject(:*)
sum = 0
a.each { |i|
  sum += b / i
}
puts 1.0 * b / sum

もしくは
n = gets.to_i
a = gets.split.map(&:to_i)
sum = a.map { |i| 1.0 / i}.sum
puts (1.0 / sum)
```
