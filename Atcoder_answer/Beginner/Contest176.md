- A問題(https://atcoder.jp/contests/abc176/tasks/abc176_a)

```
n, x, t = gets.split.map(&:to_i)

puts (n.to_f / x).ceil * t
```

- B問題
```
n = gets.chomp.chars
m = []
n.each { |i|
  m << i.to_i
}
puts m.sum % 9 == 0 ? "Yes" : "No"

# 上記ではなく『整数nが9の倍数である事とと、nを十進法で表した時の各桁の数の和が9の倍数である事は同値』と問題文にあるので下記でOKだった
n = gets.to_i
puts n % 9 == 0 ? "Yes" : "No"
```

- C問題
```
n = gets.to_i
a = gets.split.map(&:to_i)
# 自分より背の高い人が前にいる時、自分は踏み台を使って背を高くする
# 自分の背が高くなる事により、後ろの人が「背が低いままで良い」などの得はしない
# 逆に後ろの人が踏み台を使わないといけなくなる事が起こりうる
max = 0
sum = 0
a.each { |i|
  if i < max
    sum += max - i
    i = max
  end
  if i > max
    max = i
  end
}
puts sum
```
