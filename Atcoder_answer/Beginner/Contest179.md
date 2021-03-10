- A問題(https://atcoder.jp/contests/abc179/tasks/abc179_a)

```
# 自分の回答
S = gets.to_s

if /S$/ == "e"
  puts "S" + "es"
else
  puts "S" + "s"
end
なぜか正規表現を使って一致させようと考えていた…
```

- 「入力された文字列の最後の1文字」を見て条件分岐する必要がある。
- 「文字列のi番目の文字」を得る方法を使う。

```
s = gets.chomp
puts s[-1] == "s" ? s + "es" : s + "s"
```

- B問題
```
n = gets.to_i
ab = n.times.map { gets.split.map(&:to_i)}
cnt = 0
ab.each { |i, j|
  if i == j
    cnt += 1
  else
    cnt = 0
  end
  if cnt == 3
    puts "Yes"
    exit
  end
}
puts "No"
```

- C問題
```
n = gets.to_i
# a * b < n を満たす正整数の組(a, b)に対し、a * b + c = n となるような正整数cはちょうど一つに定まる
# aを固定した時、bとして考えられる値は、n - 1 / a 個 = aを1からn-1まで全探索する
cnt = 0
(1..n-1).each { |a|
  cnt += (n - 1) / a
}
puts cnt
```
