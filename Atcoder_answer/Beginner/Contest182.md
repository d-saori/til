- A問題（https://atcoder.jp/contests/abc182/tasks/abc182_a）

```
a, b = gets.split.map(&:to_i)

puts (2 * a + 100) - b
```

<br>

- B問題（https://atcoder.jp/contests/abc182/tasks/abc182_b）
```
n = gets.to_i
a = gets.split.map(&:to_i)
puts (2..1000).max_by { |k| a.count { |a| a % k == 0 }}

# 別解
n = gets.to_i
a = gets.split.map(&:to_i)
# a.max以上のkはGCD度0になるので1000まで全探索しなくても良い
puts (2..a.max).max_by { |i| a.count { |a| a % i == 0} }
```

- C問題
```
n = gets.to_i
m = n.digits
k = m.size
k.downto(1) { |i|
  m.combination(i) { |j|
    if j.sum % 3 == 0
      puts k - i
      exit
    end
  }
}
puts -1
```
