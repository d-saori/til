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
a, b = gets.chomp.split
cnt = 0
(a..b).each { |i| 
  cnt += 1 if i == i.chars.reverse.join
}
puts cnt

# 別解
a, b = gets.chomp.split
puts (a..b).select { |i| i == i.reverse }.count
```
