- A問題（https://atcoder.jp/contests/abc096/tasks/abc096_a）
```
# 自分の回答(WA✖︎1で不正解)
a, b = gets.split.map(&:to_i)
sum = 0
(1..a).each { |i|
  (1..b).each { |j|
    if i == j
      sum += 1
    end
  }
}
puts sum

# 正解
a, b = gets.split.map(&:to_i)
# 月と日付が同じなら月の値、日付が月より小さければ月-1の値
# 例5/5なら(1/1,2/2,3/3,4/4,5/5)5、5/4なら(1/1,2/2,3/3,4/4)4
puts a <= b ? a : a - 1
```

- B問題（https://atcoder.jp/contests/abc096/tasks/abc096_b）
```
ary = gets.split.map(&:to_i).sort
k = gets.to_i 
puts ary[-1] * (2 ** k) + (ary[0..-2].sum)
```
