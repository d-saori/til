- A問題（https://atcoder.jp/contests/agc025/tasks/agc025_a）
```
n = gets.chomp
if n.to_i % 10 == 0
  puts 10
else
  puts n.chars.map(&:to_i).inject(:+)
end
```
