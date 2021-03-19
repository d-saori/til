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

- C問題
```
x = gets.to_i
while true
  (2..x).each { |i|
    if i == x
      puts x
      exit
    end
    break if x % i == 0
  }
  x += 1
end

# 別解
require 'prime'
x = gets.to_i
until x.prime?
  x += 1
end
puts x
```
