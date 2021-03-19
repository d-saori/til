- A問題（https://atcoder.jp/contests/abc149/tasks/abc149_a）

```
s, t = gets.split
puts "#{t}#{s}"

# 別解答
s, t = gets.split
puts t + s

puts gets.split.reverse.join
```

- B問題
```
a, b, k = gets.split.map(&:to_i)
if a < k
  if b - (k - a) < 0
    puts [0, 0].join(" ")
  else
    puts [0, b - (k - a)].join(" ")
  end
else
  puts [a - k, b]
end

# 別解
a, b, k = gets.split.map(&:to_i)
if a + b <= k
  puts "0 0"
  exit
end

if a >= k
  puts "#{a - k} #{b}"
  exit
end

puts "0 #{b - (k - a)}"
```
