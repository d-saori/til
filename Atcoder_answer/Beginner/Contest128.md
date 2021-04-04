- A問題（https://atcoder.jp/contests/abc128/tasks/abc128_a）

```
a, p = gets.chomp.split.map(&:to_i)

puts (a * 3 + p) / 2
```

- B問題（https://atcoder.jp/contests/abc128/tasks/abc128_b）
```
n = gets.to_i
rank = []
n.times { |i|
  s, p = gets.split
  p = p.to_i
  rank << [s, -p, i+1]
}
rank.sort!
rank.each { |a, b, j|
  puts j
}

# 別解
n = gets.to_i
rank = []
n.times { |i|
  s, p = gets.chomp.split
  rank << [s, p.to_i, i + 1]
}
rank.sort_by! { |a, b, j| [a, b] }
puts rank.map!(&:last)

# 別解
n = gets.to_i
rank = []
n.times { |i|
  s, p = gets.split
  rank << [s, p.to_i, i + 1]
}
rank.sort_by { |a| [a[0], -a[1]] }.each { |a|
  puts a[2]
}
```

- C問題（https://atcoder.jp/contests/abc128/tasks/abc128_c）
```
n, m = gets.split.map(&:to_i)
lights = m.times.map{gets.split.map(&:to_i)}
ps = gets.split.map(&:to_i)

cnt = (1 << n).times.count { |state|
  lights.each_with_index.all? { |(k, *switches), l|
    switches.count { |j| state[j - 1] == 1 } % 2 == ps[l]
  }
}
puts cnt

# 別解
n, m = gets.split.map(&:to_i)
ligths = m.times.map { gets.split.map(&:to_i)[1..-1] }
ps = gets.split.map(&:to_i)
ans = (2**n).times.count { |i|
  m.times.all? { |j| ligths[j].count { |k| i[k - 1] == 1 } % 2 == ps[j] }
}
puts ans
```
