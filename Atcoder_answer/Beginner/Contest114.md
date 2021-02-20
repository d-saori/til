- A問題（https://atcoder.jp/contests/abc114/tasks/abc114_a）

```
x = gets.to_i

if x == 3 || x == 5 || x == 7
  puts "YES"
else
  puts "NO"
end

または
if [7,5,3].include? x
  puts "YES"
else
  puts "NO"
end
などでもOK
```

- B問題
```
s = gets.chomp.chars
n = s.size
num = []
(n-2).times { |i|
  num << s[i, 3].join
}
t = []
num.each { |i|
  t << (i.to_i - 753).abs
}
puts t.include?(753) ? 0 : t.min

# 別解
s = gets.chomp
ans = 753
(s.size - 2).times { |i|
  ans = [ans, (s[i, 3].to_i - 753).abs].min
}
puts ans
```
