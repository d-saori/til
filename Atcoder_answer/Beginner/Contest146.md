- A問題（https://atcoder.jp/contests/abc146/tasks/abc146_a）

```
s = gets.chomp
days = ["SUN", "MON", "TUE", "WED", "THU", "FRI", "SAT"]
# indexメソッド：条件に一致する最初の要素の位置を返す
index = days.index(s)
puts index == 0 ? 7 : 7 - index

# 省略系
puts 7 - ["SUN", "MON", "TUE", "WED", "THU", "FRI", "SAT"].index(gets.chomp)
```
