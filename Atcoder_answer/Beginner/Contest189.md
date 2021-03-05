- A問題
```
s = gets.chomp.chars
puts s.uniq.size == 1 ? "Won" : "Lost"
```

- B問題
```
n, x = gets.split.map(&:to_i)
vp = n.times.map { gets.split.map(&:to_i) }
cnt = 0
sum = 0
(1..n).each { |i|
  # al = 1杯のアルコール量
  # al = vp[i - 1][0] * (vp[i - 1][1] / 100.to_f)
  # 答えに誤差を出さない為に整数のみで計算する(100をかける)
  al = vp[i - 1][0] * vp[i - 1][1]
  sum += al
  if sum > x * 100
    break
  else
    cnt += 1
  end
}
puts cnt == n ? -1 : cnt + 1

# 別解
n, x = gets.split.map(&:to_i)
sum = 0
(1..n).each { |i|
  v, p = gets.split.map(&:to_i)
  sum += v * p
  if sum > x * 100
    puts i
    exit
  end
}
puts -1
```

- C問題
```
# l(区間の最初)を固定しrを伸ばして全探索
n = gets.to_i
a = gets.split.map(&:to_i)
ans = 0
(0..n-1).each { |l|
  min = a[l]
  (l..n-1).each { |r|
    min = [min, a[r]].min
    c = (r - l + 1) * min
    ans = [ans, c].max
    break if min * (n - l) <= ans
  }
}
puts ans

# 別解
n = gets.to_i
a = gets.split.map(&:to_i)
ans = a.max
i = 0
while i < n - 1
  min = a[i]
  j = i + 1
  while j < n
    break if min * n <= ans
    min = a[j] if min > a[j]
    ans = [ans, (j - i + 1) * min].max
    j += 1
  end
  i += 1
end
puts ans
```
