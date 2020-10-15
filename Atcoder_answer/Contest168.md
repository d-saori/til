- A問題(https://atcoder.jp/contests/abc168/tasks/abc168_a)

```
N = gets.to_i

puts "hon" if N.match?(/\z == 2, 4, 5, 7, 9/)
puts "pon" if N.match?(/\z == 0, 1, 6, 8/)
puts "bon" if N.match?(/\z == 3/)
```
