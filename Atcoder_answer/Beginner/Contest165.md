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

# each文を使わない書き方
k = gets.to_i
a, b = gets.split.map(&:to_i)
# b以下内で最大のkの倍数がa以下ならOKとなる
puts (b / k) * k >= a ? "OK" : "NG"
```
