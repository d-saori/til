- A問題（https://atcoder.jp/contests/abc122/tasks/abc122_a）

```
b = gets.chomp

if b == "A"
  puts "T"
elsif b == "T"
  puts "A"
elsif b == "C"
  puts "G"
else
  puts "C"
end
```

- B問題（https://atcoder.jp/contests/abc122/tasks/abc122_b）
```
s = gets
a = s.scan(/[ACGT]+/).map{ |i| i.size }
puts a.size == 0 ? 0 : a.max

# 別解
s = gets.chomp
puts s.scan(/[ACGT]*/).map(&:size).max

# 別解
s = gets.chomp
puts s.scan(/[ACGT]*/).map {|i| i.size }.max
```

- C問題
```
# 「右隣がCであるA」を数える
n, q = gets.split.map(&:to_i)
s = gets.chomp
t = [0] * n
n.times { |i|
  t[i+1] = t[i] + ((s[i..(i+1)] == "AC") ? 1 : 0)
}
q.times {
  l, r = gets.split.map(&:to_i)
  puts t[r-1] - t[l-1]
}

# 別解
# 「右隣がCであるA」を数える
n, q = gets.split.map(&:to_i)
s = gets.chomp
t = [0] * n
(n-1).times { |i|
  if s[i] == "A" && s[i+1] == "C"
    t[i+1] += 1
  end
  t[i+1] += t[i]
}
q.times {
  l, r = gets.split.map(&:to_i)
  puts t[r-1] - t[l-1]
}
```
