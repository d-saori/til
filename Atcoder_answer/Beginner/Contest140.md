- A問題（https://atcoder.jp/contests/abc140/tasks/abc140_a）

```
n = gets.to_i
puts n ** 3
```

- B問題
```
n = gets.to_i
a = gets.split.map(&:to_i)
b = gets.split.map(&:to_i)
c = gets.split.map(&:to_i)
ans = 0
n.times { |i|
  if i >= 1 && a[i] == a[i-1] + 1
    ans += b[a[i]-1] + c[a[i]-2]
  else
    ans += b[a[i]-1]
  end
}
puts ans

# 別解
n = gets.to_i
a = gets.split.map(&:to_i)
b = gets.split.map(&:to_i)
c = gets.split.map(&:to_i)
ans = b.sum
n.times { |i|
  ans += c[a[i] - 1] if a[i] + 1 == a[i + 1]
}
puts ans

# 別解
n = gets.to_i
a = gets.split.map(&:to_i)
b = gets.split.map(&:to_i).sum
c = gets.split.map(&:to_i)
s = 0
n.times { |i|
  s += c[a[i - 1] - 1] if i > 0 && a[i] - a[i - 1] == 1
}
puts b + s
```
