- A問題（https://atcoder.jp/contests/abc132/tasks/abc132_a）

```
s = gets.chomp
if s.split("").uniq.length == 2
  puts "Yes"
else
  puts "No"
end
```

- B問題
```
n = gets.to_i
p = gets.split.map(&:to_i)
cnt = 0
p.each_cons(3) { |i|
  j = i.sort
  cnt += 1 if i[1] == j[1]
}
puts cnt

# 別解
n = gets.to_i
p = gets.split.map(&:to_i)
puts p.each_cons(3).count { |i| i[1] == i.sort[1] }
```

- C問題
```
# 「n/2番目に難しい問題:ARC用の問題、n/2-1番目に難しい問題:ABC用の問題」と「ARC用の問題の数とABC用の問題の数が同じ」は同値
n = gets.to_i
d = gets.split.map(&:to_i)
d.sort!
c = n / 2
l = d[c - 1]
r = d[c]
puts r - l
```
