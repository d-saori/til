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

- C問題
```
# 偶数回裏返されるカード：全操作終了後は表
# 奇数回裏返されるカード：全操作終了後は裏
# 各マスのカードが何回裏返されるかを考える
n, m = gets.split.map(&:to_i)
if n == 1 && m == 1
  puts 1
elsif n == 1
  puts m - 2
elsif m == 1
  puts n - 2
else
  puts (n - 2) * (m - 2)
end
```
