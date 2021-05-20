- A問題（https://atcoder.jp/contests/abc072/tasks/abc072_a）
```
x, t = gets.split.map(&:to_i)
if x < t
  puts 0
else
  puts x - t
end
```

- B問題（https://atcoder.jp/contests/abc072/tasks/abc072_b）
```
s = gets.chomp.chars
puts s.each_slice(2).to_a.map(&:first).join

# 別解
s = gets.chomp.chars
puts s.select.with_index { |c, i| i.even? }.join
```

- C問題（https://atcoder.jp/contests/abc072/tasks/arc082_a）
```
n = gets.to_i
a = gets.split.map(&:to_i)
r = Hash.new(0)
# xを先に選んでから数に対する操作をする。この個数を最大にするには以下の3つの条件。
# 全てのx - 1に+1する
# 全てのxをそのままにする
# 全てのx + 1に-1する
# 上記をすると他は関係ないので、(x - 1の個数)+(xの個数)+(x + 1の個数)となる。
# 先に各数の個数を数えておき、このxを考えうる範囲で全て試すことで答えが求まる。
a.each { |x|
  r[x - 1] += 1
  r[x] += 1
  r[x + 1] += 1
}
puts r.values.max

# 別解
n = gets.to_i
a = gets.split.map(&:to_i)
t = Hash.new(0)
a.each { |i|
  t[i] += 1
}
ans = 0
t.each { |k, v|
  together = t[k - 1] + v + t[k + 1]
  ans = together if ans < together
}
puts ans
```
