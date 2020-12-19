- A問題（https://atcoder.jp/contests/abc150/tasks/abc150_a）

```
k, x = gets.split(" ").map(&:to_i)

if 500 * k >= x
  puts "Yes"
else
  puts "No"
end
```

- B問題（https://atcoder.jp/contests/abc150/tasks/abc150_b）
```
n = gets.to_i
s = gets
cnt = []
# 文字列sで一致した"ABC"を配列cntに追加していく
s.scan("ABC") { |i| cnt << i }
# 配列cntの長さ=一致した数
puts cnt.size

もしくは以下のようでもOK
n = gets.to_i
s = gets
puts s.scan("ABC").size
```
