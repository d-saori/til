- A問題(https://atcoder.jp/contests/abc161/tasks/abc161_a)

```
# a, b = b, a →aとbを入れ替える
# a, c = c, a →aとcを入れ替える

# 解答例１
a, b, c = gets.split(" ")
puts "#{c} #{a} #{b}"

# 解答例2
a, b, c = gets.split(" ").map(&:to_i)
puts [c, a, b].join(" ")
```
