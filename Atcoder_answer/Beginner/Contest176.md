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
