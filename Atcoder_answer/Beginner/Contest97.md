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
