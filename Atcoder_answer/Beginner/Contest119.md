- A問題（https://atcoder.jp/contests/abc119/tasks/abc119_a）

```
s = gets.chomp
puts s <= "2019/04/30" ? "Heisei" : "TBD"
```

- B問題
```
n = gets.to_i
oto = []
n.times {
  x, u = gets.chomp.split
  if u == "JPY"
    oto << x.to_i
  else
    oto << x.to_f * 380000
  end
}
puts oto.sum

# 別解
n = gets.to_i
sum = 0
n.times {
  x, u = gets.chomp.split
  sum += x.to_f * (u == "JPY" ? 1 : 380000)
}
puts sum
```
