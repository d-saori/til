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
a = gets.split.map(&:to_f)
sum = 0
a.each { |i|
  sum += 1 / i
}
puts 1.0 / sum

# 別解
n = gets.to_i
a = gets.split.map(&:to_i)
sum = a.map { |i| 1.0 / i }.sum
puts (1.0 / sum)
```
