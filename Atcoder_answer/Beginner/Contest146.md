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

- B問題
```
# 問題解く際の参考(https://qiita.com/ya-maruchoba/items/9e26c971fbaffb77c7d2)(http://www3.nit.ac.jp/~tamura/ex2/ascii.html)
n = gets.to_i
s = gets.chomp.chars
num = []
# アルファベットの大文字コード:65〜90
s.each { |i|
  c = i.ord - 65
  d = (c + n) % 26
  e = d + 65
  num << e.chr
}
puts num.join

# 別解
n = gets.to_i
s = gets.chomp.chars
a = "A".ord
puts s.map { |i| ((i.ord - a + n) % 26 + a).chr }.join
```
