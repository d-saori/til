- A問題
```
ab = gets.split.map(&:to_i)
cd = gets.split.map(&:to_i)
puts ab.max - cd.min
```

- B問題
```
require 'bigdecimal'
require 'bigdecimal/util'
x = gets.to_d
puts x.floor
```

- C問題
```
# TLEで不正解だったコード
n = gets.to_i
puts (11..n).select { |i|
  m = i.to_s.chars
  m.size.even? && m[0..m.size/2-1] == m[m.size/2..-1]
}.count

# ACのコード
# n < 10**12 の中で偶数の桁数は半分の10**6
n = gets.to_i
cnt = 0
(1..10**6).each { |i|
  cnt += 1 if (i.to_s + i.to_s).to_i <= n
}
puts cnt
```
