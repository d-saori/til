- A問題（https://atcoder.jp/contests/abc093/tasks/abc093_a）
```
s = gets.chomp.chars.sort.join
puts s == "abc" ? "Yes" : "No"
```

- B問題（https://atcoder.jp/contests/abc093/tasks/abc093_b）
```
# 自分の提出コード（不正解）
a, b, k = gets.split.map(&:to_i)
ary = []
(a..b).each { |i| ary << i}
puts k > ary.size ? ary : (ary[0..k] + ary[-k..-1]).uniq

# 正解
a, b, k = gets.split.map(&:to_i)
puts ((a..b).first(k) + (-b..-a).first(k)).map(&:abs).uniq.sort
```
