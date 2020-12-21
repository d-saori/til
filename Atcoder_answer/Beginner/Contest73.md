- A問題（https://atcoder.jp/contests/abc073/tasks/abc073_a）
```
n = gets.chomp.chars
puts n.index("9") ? "Yes" : "No"

#　他の回答1
n = gets.to_i
# 10の位:a = (n / 10) % 10
a = n / 10
# 1の位:b = (n / 1) % 10
b = n % 10
puts a == 9 || b == 9 ? "Yes" : "No"

# 他の回答2
puts gets.match(/9/) ?　"Yes" : "No"
```

- B問題（https://atcoder.jp/contests/abc073/tasks/abc073_b）
```
n = gets.to_i
guests = n.times.map{gets.split.map(&:to_i)}
sum = 0
guests.each { |l, r|
  sum += r - l + 1
}
puts sum

もしくは
n = gets.to_i
l, r = gets.split.map(&:to_i)
sum = 0
n.times {
  l, r = gets.split.map(&:to_i)
  sum += r - l + 1
}
puts sum
```

- C問題（https://atcoder.jp/contests/abc073/tasks/abc073_c）
```
# 奇数回登場する数は最後に紙に書かれているので、奇数回登場する数が何種類あるか求める
n = gets.to_i
a = n.times.map{gets.split.map(&:to_i)}.sort.flatten
puts a.group_by(&:itself).count { |k, v| v.count.odd? }
```
