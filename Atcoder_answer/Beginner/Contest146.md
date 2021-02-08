- A問題（https://atcoder.jp/contests/abc146/tasks/abc146_a）

```
s = gets.chomp
if s == "SUN"
  puts 7
elsif s == "MON"
  puts 6
elsif s == "TUE"
  puts 5
elsif s == "WED"
  puts 4
elsif s == "THU"
  puts 3
elsif s == "FRI"
  puts 2
else
  puts 1
end

# 別解
s = gets.chomp
days = ["SUN", "MON", "TUE", "WED", "THU", "FRI", "SAT"]
# indexメソッド：条件に一致する最初の要素の位置を返す
index = days.index(s)
puts index == 0 ? 7 : 7 - index

# 省略系
puts 7 - ["SUN", "MON", "TUE", "WED", "THU", "FRI", "SAT"].index(gets.chomp)
```
