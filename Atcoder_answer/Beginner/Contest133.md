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
n, d = gets.chomp.split.map(&:to_i)
a = n.times.map{gets.chomp.split.map(&:to_i)}
count = 0
(0...n).each { |i|
  (i+1...n).each { |j|
    dist_sq = (0...d).map { |di| (a[i][di] - a[j][di]) ** 2}.reduce(:+)
    dist = Math.sqrt(dist_sq)
    count = count + 1 if dist % 1 == 0
  }
}
puts count

もしくは
n, d = gets.chomp.split.map(&:to_i)
a = n.times.map{gets.chomp.split.map(&:to_i)}
count = 0

a.combination(2) { |first, second|
  sum = 0
  (0...d).each { |num| 
    sum += (first[num] - second[num]) ** 2
  }
  count += 1 if (sum ** 0.5).to_i == (sum ** 0.5)
}
puts count
など
```
