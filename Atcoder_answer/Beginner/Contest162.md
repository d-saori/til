- A問題（https://atcoder.jp/contests/abc162/tasks/abc162_a）

```
n = gets
puts n[0] == "7" || n[1] == "7" || n[2] == "7" ? "Yes" : "No"

# もしくは
n = gets
puts n.include?("7") ? "Yes" : "No"
```

- B問題
```
n = gets.to_i
num = [*1..n]
s = []
num.select { |i| s << i if i % 3 != 0 && i % 5 != 0 }
puts s.sum

# 別解
n = gets.to_i
sum = 0
(1..n).each { |i|
  sum += i if i % 5 != 0 && i % 3 != 0 
}
p sum
```

- C問題
```
k = gets.to_i
ans = 0
(1..k).to_a.repeated_permutation(3) { |a, b, c|
  ans += a.gcd(b).gcd(c)
}
puts ans

# 別解
k = gets.to_i
ans = 0
(1..k).each { |a|
  (1..k).each { |b|
    x = a.gcd(b)
    if x == 1
      ans += k
    else
      (1..k).each { |c| ans += x.gcd(c) }
    end
  }
}
puts ans
```
