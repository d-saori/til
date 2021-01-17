- A問題
```
# 猫の数は、B匹すべてが犬のときに最小 (A 匹) になり、B匹すべてが猫のときに最大 (A + B 匹) になる
a, b, x = gets.split.map(&:to_i)
puts a <= x && x <= a + b ? "YES" : "NO"
```
