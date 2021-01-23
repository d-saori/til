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
