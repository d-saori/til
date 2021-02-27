- A問題
```
a, b = gets.split.map(&:to_i)
puts (1 - (b.to_f / a.to_f)) * 100

# 別解
a, b = gets.split.map(&:to_f)
puts (1 - b / a) * 100
```

- B問題
```
n = gets.to_i
buy = []
n.times {
  a, p, x = gets.split.map(&:to_i)
  if a >= x
    buy << -1
  else
    buy << p
  end
}
if buy.each.all? { |i| i == -1 }
  puts -1
else
  buy.delete(-1)
  puts buy.min
end

# 別解
n = gets.to_i
buy = []
n.times {
  a, p, x = gets.split.map(&:to_i)
  buy << p if x > a
}
puts buy == [] ? -1 : buy.min
```

- C問題
```
n = gets.to_i
ans = []
(2..Math.sqrt(n).floor).each { |i|
  j = 2
  while i ** j <= n
    ans << i ** j
    j += 1
  end
}
puts n - ans.uniq.size
```
