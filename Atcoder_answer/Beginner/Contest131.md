- A問題（https://atcoder.jp/contests/abc131/tasks/abc131_a）

```
s = gets.chomp.to_s

if s[0] == s[1] || s[1] == s[2] || s[2] == s[3]
  puts "Bad"
else
  puts "Good"
end
```

- B問題
```
n, l = gets.split.map(&:to_i)
ary = [*1..n]
sum = ary.sum + (n * l) - (n * 1)
b = []
ary.combination(n-1) { |i|
  b << (sum - (i.sum + ((n - 1) * l) - ((n - 1) * 1))).abs
}
min = b.min
num = b.index(min)
puts ary.combination(n-1).to_a[num].sum + ((n - 1) * l) - ((n - 1) * 1)

# 別解
n, l = gets.split.map(&:to_i)
taste = []
# n個のりんごの美味しさは、l, l+1, l+2,...l+n-1
n.times { |i|
  taste << l + i
}
taste = taste.sort_by { |j| j.abs }
puts taste.sum - taste[0]
```

- C問題
```
# 全体の数(x) - cで割れる数(x/c) - dで割れる数(x/d) + cとdどちらでも割れる数(x/c.lcm(d))
# aまでで cで割り切れる数 + dで割り切れる数 - 公約数で割り切れる数
a, b, c, d = gets.split.map(&:to_i)
lcm = c.lcm(d)
a -= 1
x = a - ((a/c).to_i + (a/d).to_i - (a/lcm).to_i)
y = b - ((b/c).to_i + (b/d).to_i - (b/lcm).to_i)
puts y - x
```
