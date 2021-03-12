- A問題（https://atcoder.jp/contests/abc173/tasks/abc173_a）
```
n = gets.to_i
# 1000円札のみで支払いを行う以上、nの下3桁のみがお釣りの金額に関係する
puts (1000 - n % 1000) % 1000

# 別解
n = gets.to_f
m = (n / 1000).ceil
puts (m * 1000 - n).to_i
```

- B問題
```
n = gets.to_i
s = n.times.map { gets.chomp }
ac = 0
wa = 0
tle = 0
re = 0
s.each { |i|
  ac += 1 if i == "AC"
  wa += 1 if i == "WA"
  tle += 1 if i == "TLE"
  re += 1 if i == "RE"
}
puts "AC x #{ac}"
puts "WA x #{wa}"
puts "TLE x #{tle}" 
puts "RE x #{re}" 

# 別解
n = gets.to_i
s = n.times.map { gets.chomp }
m = ["AC", "WA", "TLE", "RE"]
puts m.map { |i| "#{i} x #{s.count(i)}" }
```

- C問題
```
h, w, k = gets.split.map(&:to_i)
c = h.times.map { gets.chomp.chars }
ans = 0
[0, 1].repeated_permutation(h).each { |i|
  [0, 1].repeated_permutation(w).each { |j|
    cnt = 0
    i.each_with_index { |a, b|
      j.each_with_index { |d, e|
        next if a == 0 || d == 0
        cnt += 1 if c[b][e] == "#"
      }
    }
    ans += 1 if cnt == k
  }
}
puts ans
```
