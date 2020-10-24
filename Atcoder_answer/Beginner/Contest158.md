- A問題（https://atcoder.jp/contests/abc158/tasks/abc158_a）

```
s = gets.chomp.to_s

if s == ("AAA" or "BBB")
  puts "No"
else
  puts "Yes"
end

としたが、orではなく論理演算子||を使う
s = gets.chomp.to_s

if s == ("AAA" || "BBB")
  puts "No"
else
  puts "Yes"
end
```
