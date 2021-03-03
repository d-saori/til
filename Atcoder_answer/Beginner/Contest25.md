- A問題
```
s = gets.chomp.chars
n = gets.chomp.to_i
r = s.repeated_permutation(2).to_a
puts r[n - 1].join

# 別解
s = gets.chomp.chars
n = gets.chomp.to_i
puts s.product(s)[n - 1].join
```

- B問題
```
n, a, b = gets.split.map(&:to_i)
e = []
w = []
n.times {
  s, d = gets.chomp.split
  if d.to_i < a
    if s == "East"
      e << a
    else
      w << a
    end
  elsif a <= d.to_i && d.to_i <= b
    if s == "East"
      e << d.to_i
    else
      w << d.to_i
    end
  else
    if s == "East"
      e << b
    else
      w << b
    end
  end
}
if e.sum == w.sum
  puts 0
elsif e.sum > w.sum
  puts ["East", e.sum - w.sum].join(" ")
else
  puts ["West", w.sum - e.sum].join(" ")
end

# 別解
n, a, b = gets.split.map(&:to_i)
h = ["East", "West"]
t = [-1, 1]
ans = 0
n.times {
  s, d = gets.chomp.split
  ans += [[a, d.to_i].max, b].min * t[h.index(s)]
}
puts (ans == 0) ? 0 : (ans > 0 ? "West #{ans}" : "East #{-ans}")
```
