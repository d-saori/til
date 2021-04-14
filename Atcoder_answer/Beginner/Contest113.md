- A問題（https://atcoder.jp/contests/abc113/tasks/abc113_a）

```
x, y = gets.split.map(&:to_i)

puts x + (y / 2)
```

- B問題（https://atcoder.jp/contests/abc113/tasks/abc113_b）
```
n = gets.to_i
t, a = gets.split.map(&:to_i)
h = gets.split.map(&:to_i)
tem = []
eria = []
# 不動小数点型を用いないように気温を1000倍する
n.times { |i|
  tem << 1000 * t - h[i] * 6
}
tem.each { |j|
  eria << (1000 * a - j).abs
}
min = eria.min
puts eria.index(min) + 1

# 別解
n = gets.to_i
t, a = gets.split.map(&:to_i)
h = gets.split.map(&:to_i)

puts (1..n).min_by { |x| (a - t + h[x - 1] * 0.006).abs }
```

- C問題
```
n, m = gets.split.map(&:to_i)
arr = []
hash = {}
m.times {
  pi, yi = gets.split.map(&:to_i)
  hash[pi] ||= {}
  hash[pi][yi] = true
  arr << [pi, yi]
}
hash.keys.sort.each { |pi|
  h = hash[pi]
  h.keys.sort.each_with_index { |yi, i|
    h[yi] = i + 1
  }
}
arr.each { |pi, yi|
  puts "00000#{pi}"[-6..-1] + "00000#{hash[pi][yi]}"[-6..-1]
}
```
