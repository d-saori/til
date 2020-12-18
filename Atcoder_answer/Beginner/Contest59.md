- A問題（https://atcoder.jp/contests/abc059/tasks/abc059_a）
```
s = gets.split.map(&:to_s)
puts s.map { |i| i[0] }.join.upcase
```

- B問題（https://atcoder.jp/contests/abc059/tasks/abc059_b）
```
a = gets.to_i
b = gets.to_i
if a > b
  puts "GREATER"
elsif a < b
  puts "LESS"
else
  puts "EQUAL"
end
```

-　C問題（https://atcoder.jp/contests/abc059/tasks/arc072_a）
```
n = gets.to_i
a = gets.split.map(&:to_i)

# 最初の要素a[0]を正にする
sign = 1
sum = 0
ope1 = 0
a.each { |i|
  sum += i
  if sum * sign <= 0
    ope1 += (sign - sum).abs
    sum = sign
  end
  sign *= -1
}

# 最初の要素a[0]を負にする
sign = -1
sum = 0
ope2 = 0
a.each { |i|
  sum += i
  if sum * sign <= 0
    ope2 += (sign - sum).abs
    sum = sign
  end
  sign *= -1
}

puts [ope1, ope2].min
```
