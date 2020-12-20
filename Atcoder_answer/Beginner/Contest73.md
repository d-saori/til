- A問題（https://atcoder.jp/contests/abc073/tasks/abc073_a）
```
n = gets.chomp.chars
puts n.index("9") ? "Yes" : "No"

#　他の回答1
n = gets.to_i
# 10の位:a = (n / 10) % 10
a = n / 10
# 1の位:b = (n / 1) % 10
b = n % 10
puts a == 9 || b == 9 ? "Yes" : "No"

# 他の回答2
puts gets.match(/9/) ?　"Yes" : "No"
```
