- A問題（https://atcoder.jp/contests/abc134/tasks/abc134_a）

```
r = gets.to_i
puts 3 * (r ** 2)
```

- B問題
```
n, d = gets.split.map(&:to_i)
# 監視員1人は、2D+1の木を監視できる
# 2D+1=WとしたらN本の木を監視する人数はN/W
w = 2 * d + 1
puts (n / w.to_f).ceil

# 別解
n, d = gets.split.map(&:to_i)
ans = 0
while true
  if ans * (2 * d + 1) >= n
    puts ans
    break
  else
    ans += 1
  end
end
```

- C問題
```
# TLEになったコード
n = gets.to_i
a = n.times.map { gets.to_i }
n.times { |i|
  b = []
  a.select.with_index { |num, idx|
    b << num if idx != i
  }
  puts b.max
}

# 別解
n = gets.to_i
a = n.times.map { gets.to_i }
b = a.sort
a.map { |i|
  puts i == b[-1] ? b[-2] : b[-1]
}

# 別解
# 取り除かれる値AiがAmaxと等しい以外は、2番目に大きい値になる
n = gets.to_i
a = n.times.map { gets.to_i }
b = a.max(2)
puts a.map { |i| i == b[0] ? b[1] : b[0] }
```
