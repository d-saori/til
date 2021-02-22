- A問題（https://atcoder.jp/contests/abc097/tasks/abc097_a）

```
# absメソッド：数値から絶対値を求める
a, b, c, d = gets.split.map(&:to_i)
if (a - c).abs <= d || (a - b).abs <= d && (b - c).abs <= d
  puts "Yes"
else
  puts "No"
end
```

- B問題
```
x = gets.to_i
ans = 1
(1..x).each { |i|
  (2..10).each { |j|
    k = i ** j
    break if k > x
    ans = k if ans < k
  }
}
puts ans
```
