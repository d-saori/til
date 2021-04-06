- A問題（https://atcoder.jp/contests/abc126/tasks/abc126_a）

```
n, k = gets.split.map(&:to_i)
s = gets
s[k - 1] = s[k - 1].downcase
puts s

# 別解
n, k = gets.split.map(&:to_i)
s = gets.chomp.chars
s[k-1].downcase!
puts s.join
```

- B問題
```
s = gets.chomp
a = s[0, 2].to_i
b = s[2, 2].to_i
yymm = 1 <= b && b <= 12
mmyy = 1 <= a && a <= 12
if yymm && mmyy
  puts "AMBIGUOUS"
elsif yymm
  puts "YYMM"
elsif mmyy
  puts "MMYY"
else
  puts "NA"
end

# 別解
s = gets.chomp
m = s[0..1].to_i
n = s[2..3].to_i
w = ["NA", "YYMM", "MMYY", "AMBIGUOUS"]
x = (1 <= m && m <= 12) ? 2 : 0
y = (1 <= n && n <= 12) ? 1 : 0
puts w[x + y]
```

- C問題
```
n, k = gets.split.map(&:to_f)
ans = 0
(1..n).each { |i|
  j = 1 / n
  while i < k
    i *= 2
    j /= 2
  end
  ans += j
}
puts ans
```
