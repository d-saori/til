- A問題（https://atcoder.jp/contests/abc133/tasks/abc133_a）

```
n, a, b = gets.split.map(&:to_i)
r = n * a

puts [r, b].min

と回答しACだったが、変数rの下りはいらず

n, a, b = gets.split.map(&:to_i)

puts [n * a, b].min

でOK
```

- B問題（https://atcoder.jp/contests/abc133/tasks/abc133_b）
```
n, d = gets.split.map(&:to_i)
x = n.times.map { gets.split.map(&:to_i) }
cnt = 0
x.combination(2) { |i, j| 
  sum = 0
  (0...d).each { |num|
    sum += (i[num] - j[num]) ** 2
  }
  cnt += 1 if (sum ** 0.5).to_i == (sum ** 0.5)
}
puts cnt
```
