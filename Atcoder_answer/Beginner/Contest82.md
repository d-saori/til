- A問題（https://atcoder.jp/contests/abc082/tasks/abc082_a）
```
a, b = gets.split.map(&:to_f)
puts ((a + b) / 2).ceil
```

- B問題（https://atcoder.jp/contests/abc082/tasks/abc082_b）
```
s, t = 2.times.map { gets.chomp }
sa = s.chars.sort.join
ta = t.chars.sort.reverse.join
puts sa < ta ? "Yes" : "No"

# さらに省略
s = gets.chomp.chars.sort.join
t = gets.chomp.chars.sort.reverse.join
puts s < t ? "Yes" : "No"
```

- C問題
```
n = gets.to_i
a = gets.split.map(&:to_i)
m = Hash.new(0)
a.each { |i|
  m[i] += 1
}
ans = 0
m.each { |k, v|
  if v < k
    ans += v
  else
    ans += v - k
  end
}
puts ans
```
