- A問題（https://atcoder.jp/contests/abc115/tasks/abc115_a）

```
d = gets.to_i
if d == 25
  puts "Christmas"
elsif d == 24
  puts "Christmas Eve"
elsif d == 23
  puts "Christmas Eve Eve"
else d == 22
  puts "Christmas Eve Eve Eve"
end

# 別解
d = gets.to_i
puts "Christmas" + "Eve" * (25 - d)
```

- B問題
```
n = gets.to_i
p = n.times.map { gets.to_i }.sort.reverse
puts p[0] / 2 + p[1..-1].sum

# 別解
n = gets.to_i
p = n.times.map { gets.to_i }
puts p.sum - p.max / 2
```

- C問題
```
# 最も高い木と最も低い木の高さの差を近づけるには、低い順に並べたk本の隣り合った木を飾るべき
# 「左から1,2,..k本目」「左から2,3,..k+1本目」「n-k+1,n-k+2,..n本目」
n, k = gets.split.map(&:to_i)
h = n.times.map { gets.to_i }.sort
ans = 10 ** 9
(n-k+1).times { |i|
  n = h[i+k-1] - h[i]
  ans = n if n < ans
}
puts ans
```
