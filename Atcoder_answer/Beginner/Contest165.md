- A問題（https://atcoder.jp/contests/abc165/tasks/abc165_a）
```
k = gets.to_i
a, b = gets.split.map(&:to_i)
ans = "NG"
(a..b).each { |i|
  if i % k == 0
    ans = "OK"
  else
    ans
  end
}
puts ans

# 別解
k = gets.to_i
a, b = gets.split.map(&:to_i)
cnt = 0
(a..b).each { |i|
  cnt += 1 if i % k == 0
}
puts cnt >= 1 ? "OK" : "NG"

# each文を使わない書き方
k = gets.to_i
a, b = gets.split.map(&:to_i)
# b以下内で最大のkの倍数がa以下ならOKとなる
puts (b / k) * k >= a ? "OK" : "NG"
```

- B問題
```
x = gets.to_i
now = 100
sum = 0
while now < x
  now = (now * 1.01).floor
  sum += 1
end
puts sum
```

- C問題
```
n, m, q = gets.split.map(&:to_i)
abcd = q.times.map { gets.split.map(&:to_i) }
max = 0
[*1..n+m-2].combination(n-1) { |per|
  mi = [1]
  (n-1).times { |i|
    mi << per[i] - i
  }
  cnt = 0
  abcd.each { |a, b, c, d|
    cnt += 1 if mi[b-1] - mi[a-1] == c
  }
  max = cnt if cnt > max
}
puts max

# 別解
n, m, q = gets.split.map(&:to_i)
nums = q.times.map { gets.split.map(&:to_i) }
options = [*1..m]
ans = []
options.repeated_combination(n).each { |combi|
  ary = combi.to_a
  tmp = 0
  nums.each { |a, b, c, d|
    if ary[b - 1] - ary[a - 1] == c
      tmp += d
    end
  }
  ans << tmp
}
puts ans.max
```
