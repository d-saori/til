- A問題（https://atcoder.jp/contests/abc147/tasks/abc147_a）

```
a, b, c = gets.split.map(&:to_i)

if (a + b + c) >= 22
  puts "bust"
else
  puts "win"
end
```

- B問題
```
s = gets.chomp
n = s.size
cnt = 0
n.times { |i|
  j = n - 1 - i
  break if i >= j
  if s[i] != s[j]
    cnt += 1
  end
}
puts cnt

# 別解
s = gets.chomp.chars
puts s.count { |i| i != s.pop }
```

- C問題
```
# n人の人がそれぞれ正直者か否かについては全部で2**n通り
# 0以上2**n未満の整数jが「1以上n以下の整数kについて、人kが正直者であることと、jを2進数表記した際にk-1桁目が1である事が同値」
n = gets.to_i
people = n.times.map {
  a = gets.to_i
  a.times.map {
    x, y = gets.split.map(&:to_i)
    [x-1, y]
  }
}
max = 0
(1 << n).times { |c|
  test = [nil] * n
  if n.times.all? { |i|
    next true if c[i] == 0
    people[i].all? { |(x, y)|
      next false if test[x] and test[x] != y or c[x] != y
      test[x] = y
      true
      }
    }
    cnt = n.times.count { |i| c[i] == 1 }
    max = [max, cnt].max
  end
}
puts max
```
