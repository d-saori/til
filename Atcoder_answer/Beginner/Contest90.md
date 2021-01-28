- A問題（https://atcoder.jp/contests/abc090/tasks/abc090_a）
```
ca = gets.chomp.split("")
cb = gets.chomp.split("")
cc = gets.chomp.split("")
puts ca[0] + cb[1] + cc[2]

# 省略したコード
puts gets[0] + gets[1] + gets[2]
```

- B問題（https://atcoder.jp/contests/abc090/tasks/abc090_b）
```
a, b = gets.split.map(&:to_i)
cnt = 0
(a..b).each { |i|
  cnt += 1 if i.to_s == i.to_s.reverse
}
puts cnt
```
