- A問題（https://atcoder.jp/contests/abc114/tasks/abc114_a）

```
x = gets.to_i

if x == 3 || x == 5 || x == 7
  puts "YES"
else
  puts "NO"
end

または
if [7,5,3].include? x
  puts "YES"
else
  puts "NO"
end
などでもOK
```

- B問題
```
s = gets.chomp.chars
n = s.size
num = []
(n-2).times { |i|
  num << s[i, 3].join
}
t = []
num.each { |i|
  t << (i.to_i - 753).abs
}
puts t.include?(753) ? 0 : t.min

# 別解
s = gets.chomp
ans = 753
(s.size - 2).times { |i|
  ans = [ans, (s[i, 3].to_i - 753).abs].min
}
puts ans
```

- C問題
```
n = gets.to_i
a = ["3", "5", "7"]
cnt = 0
3.step(9) { |i|
  cnt += a.repeated_permutation(i).count { |j|
    j.uniq.size == 3 && j.hoin.to_i <= n
  }
}
puts cnt

# 別解
N = gets.to_i
$cnt = 0
def f(n)
  if n > N
    return
  else
    s = "#{n}"
    $cnt += 1 if s[?7] && s[?5] && s[?3]
    f(n * 10 + 7)
    f(n * 10 + 5)
    f(n * 10 + 3)
  end
end
f 0
puts $cnt
```
