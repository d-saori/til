- A問題（https://atcoder.jp/contests/abc148/tasks/abc148_a）

```
a = gets.to_i
b = gets.to_i

all = [1, 2, 3]
all.delete(a)
all.delete(b)
puts all

# 別解答
a = gets.to_i
b = gets.to_i
puts 6 - (a + b)
```

- B問題（https://atcoder.jp/contests/abc148/tasks/abc148_b）
```
n = gets.to_i
s, t = gets.split
puts s.chars.zip(t.chars).join

# 別解
n = gets.to_i
s, t = gets.chomp.split
st = []
n.times { |i|
  st << s[i]
  st << t[i]
}
puts st.join
```

- C問題（https://atcoder.jp/contests/abc148/tasks/abc148_c）
```
a, b = gets.split.map(&:to_i)
puts a.lcm(b)
```

- D問題
```
n = gets.to_i
a = gets.split.map(&:to_i)
# 任意のレンガを砕いて1,2,3..と順列が作れるかどうか判定する
# 1が無ければ-1
cnt = 0
a.each { |i|
  cnt += 1 if cnt + 1 == i
}
puts cnt == 0 ? -1 : n - cnt
```
