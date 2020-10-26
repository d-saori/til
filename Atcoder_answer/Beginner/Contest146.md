- A問題（https://atcoder.jp/contests/abc146/tasks/abc146_a）

```
# arry = ["SUN", "MON", "TUE", "WED", "THU", "FRI", "SAT"]
arry = %w(SUN MON TUE WED THU FRI SAT)
s = gets.chomp

# indexメソッド：条件に一致する最初の要素の位置を返す
puts 7 - arry.index(s)
```
