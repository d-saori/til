- A問題（https://atcoder.jp/contests/abc167/tasks/abc167_a）
```
s = gets.chomp
t = gets.chomp
puts s[0..-1] == t[0..-2] ? "Yes" : "No"

もしくは
s = gets.chomp
t = gets.chomp
puts t.match?(/^#{s}.$/) ? 'Yes' : 'No'
```

- B問題
```
a, b, c, k = gets.split.map(&:to_i)
if a >= k
  puts k
elsif a + b >= k
  puts a
else
  puts a - (k - a - b)
end

# 別解
a, b, c, k = gets.split.map(&:to_i)
# 1が書いてあるaのカードは全部選ぶ
# 次に0が書いてあるbのカードを選ぶ
# 最後に-1が書いてあるcのカードを選ぶ
if a >= k
  puts k
elsif a + b >= k
  puts a
else
  puts a - (k - (a + b)) #=> # cのカードには-1が書いてある:(k - (a + b)) = cの枚数なのでa - c
end
```

- C問題
```
n, m, x = gets.split.map(&:to_i)
ca = n.times.map { gets.split.map(&:to_i) }
ans = []
te = [*1..n].map { |i| ca.combination(i).to_a }.flatten(1)
te.each { |i|
  a = i.to_a.transpose.map(&:sum)
  ans << a[0] if a[1..m].all? { |p| p >= x }
}
puts ans.size.zero? ? -1 : ans.min
```
