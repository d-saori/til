- A問題(https://atcoder.jp/contests/abc161/tasks/abc161_a)

```
x, y, z = gets.split.map(&:to_i)
puts "#{z} #{x} #{y}"

# 別解答例
x, y, z = gets.split(" ").map(&:to_i)
puts [z, x, y].join(" ")
```
