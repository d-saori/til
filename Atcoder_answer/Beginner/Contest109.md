- A問題（https://atcoder.jp/contests/abc109/tasks/abc109_a）

```
a, b = gets.split.map(&:to_i)
# a * bの値が偶数ならcが偶数でも奇数でも答えは偶数になる
if a * b % 2 == 0
  puts "No"
else
  puts "Yes"
end
```
