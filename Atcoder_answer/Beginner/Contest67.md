- A問題（https://atcoder.jp/contests/abc067/tasks/abc067_a）
```
a, b = gets.split.map(&:to_i)
if a % 3 == 0 || b % 3 == 0 || (a + b) % 3 == 0
  puts "Possible"
else
  puts "Impossible"
end
```

- B問題（https://atcoder.jp/contests/abc067/tasks/abc067_b）
```
n, k = gets.chomp.split.map(&:to_i)
ary = gets.split.map(&:to_i).sort!.reverse!
puts ary[0..k - 1].sum
```
