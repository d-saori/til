- A問題（https://atcoder.jp/contests/abc173/tasks/abc173_a）


```
N = gets.chomp.to_i

if N % 1000 == 0
  puts 0
else
  puts 1000 - (N % 1000)
end
```
