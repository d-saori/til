- A問題（https://atcoder.jp/contests/abc142/tasks/abc142_a）

```
n = gets.to_f
puts (n / 2.0).ceil / n

# 別解
n = gets.to_i
if n.odd?
  p (n / 2 + 1) / n.to_f
else 
  p (n / 2) / n.to_f
end

# 別解
n = gets.to_i
odd = []
[*1..n].each { |i|
  if i % 2 != 0
    odd << i
  end
}
puts odd.size / n.to_f
```

- B問題
```
n, k = gets.split.map(&:to_i)
h = gets.split.map(&:to_i)
cnt = 0
h.each { |i|
  cnt += 1 if i >= k
}
puts cnt

# 別解
n, k = gets.split.map(&:to_i)
h = gets.split.map(&:to_i)
puts h.count { |i| i >= k }
```

- C問題
```
n = gets.to_i
a = gets.split.map(&:to_i)
ary = Array.new(n)
n.times { |i|
  ary[a[i]-1] = i + 1
}
puts ary.join(" ")

# 別解
n = gets.to_i
a = gets.split.map(&:to_i)
a.each_with_index { |i, idx|
  a[i - 1] = idx + 1
}
puts a.join(" ")
```
