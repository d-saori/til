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

- B問題
```
n = gets.to_i
w = n.times.map { gets.chomp }
cnt = 0
w.each_cons(2) { |a, b|
  cnt += 1 if a[-1] != b[0]
}
puts cnt == 0 && w.uniq.size == w.size ? "Yes" : "No"
```
