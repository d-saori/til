- A問題（https://atcoder.jp/contests/abc101/tasks/abc101_a）

```
s = gets.chomp.chars
p = s.count("+")
m = s.count("-")
puts (p - m)

# 別解
s = gets.chomp
ans = 0
4.times do |i|
  ans += 1 if s[i] == "+"
  ans -= 1 if s[i] == "-"
end
puts ans

または
s = gets.chomp.split('')
ans = 0
s.each do |i|
  if i == "+"
    ans += 1
  else
    ans -= 1
  end
end
puts ans
```

- B問題
```
n = gets
a = n.chars.map { |i| i.to_i }.inject(:+)
puts n.to_i % a == 0 ? "Yes" : "No"
```
