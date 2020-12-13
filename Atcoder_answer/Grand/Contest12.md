- A問題（https://atcoder.jp/contests/agc012/tasks/agc012_a）
```
n = gets.to_i
a = gets.split.map(&:to_i).sort.reverse
sum = 0

a[0, 2 * n].each_slice(2) { |i|
  sum += i[1]
}
puts sum
```
