- A問題（https://atcoder.jp/contests/abc186/tasks/abc186_a）
```
n, w = gets.split.map(&:to_i)
puts n / w
```

- B問題（https://atcoder.jp/contests/abc186/tasks/abc186_b）
```
# 自分の提出したコード不正解(sampleAll:AC、他4ACだがWA。ブロックの値が2種類以上の場合を考えてなかったのと、そもそもブロックの最小値を求めて考えればよかった)
h, _w = gets.split.map(&:to_i)
a = h.times.map{gets.split.map(&:to_i)}.flatten
 
# 個数が一番少ない要素を取得
b = a.min_by { |i| a.count(i) }
# 個数が一番多い要素を取得
c = a.max_by { |j| a.count(j)}

# ブロックの値が全部同じ時
if a.uniq.count == 1
  puts 0
elsif b > 0
  puts (b - c).abs * a.grep(b).count
else
  puts (b - c).abs * a.grep(c).count
end


# 最初に最小値を求め、各要素から最小値を引いたものの和を計算すればよい
# 解説見てからの自分のコード(正解)
h, _w = gets.split.map(&:to_i)
a = h.times.map{gets.split.map(&:to_i)}.flatten
b = a.min
new_a = []
new_a = a.map { |i| i - b }
puts new_a.sum

# 他の回答
h, w = gets.split.map(&:to_i)
a = h.times.map{gets.split.map(&:to_i)}.flatten
puts a.sum - a.min * h * w
```

- C問題
```
n = gets.to_i
cnt = 0
(1..n).each { |i|
  z = i.to_s(10)
  h = i.to_s(8)
  cnt += 1 if z.include?("7") || h.include?("7")
}
puts [*1..n].size - cnt

# 別解
n = gets.to_i
cnt = 0
(1..n).each { |i|
  cnt += 1 unless i.to_s.include?("7") || i.to_s(8).include?("7")
}
puts cnt

# 別解
n = gets.to_i
cnt = 0
i = 1
while i <= n
  cnt += 1 unless i.to_s.include?("7") || i.to_s(8).include?("7")
  i += 1
end
puts cnt
```
