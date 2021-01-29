- A問題（https://atcoder.jp/contests/abc071/tasks/abc071_a）
```
s = gets.chomp.chars
puts s.count("1")
```

- B問題（https://atcoder.jp/contests/abc071/tasks/abc071_b）
```
n = gets.to_i
a = gets.split.map(&:to_i)
cnt = 0
while a.all?(&:even?)
  a = a.map { |i| i / 2 }
  cnt += 1
end
puts cnt
```

- C問題（https://atcoder.jp/contests/abc081/tasks/arc086_a）
```
n, k = gets.split.map(&:to_i)
a = gets.split.map(&:to_i).sort
ans = 0

if (num = a.uniq.count) > k
  b = a.group_by(&:itself).map{ |k, v| [k, v.count] }.sort_by(&:last)
  (num - k).times {|i|
    ans += b[i][1]
  }
end

puts ans
```
