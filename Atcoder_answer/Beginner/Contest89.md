- A問題
```
n = gets.to_i
puts n / 3
```

- B問題
```
n = gets.to_i
s = gets.chomp.split
t = []
s.each { |i|
  t << i
}
puts t.uniq.size == 3 ? "Three" : "Four"

# 別解
n = gets.to_i
s = gets.chomp.split
puts s.index("Y") ? "Four" : "Three"
```

- C問題
```
# 名前がMから始まる人:m人、Aから始まる人:a人、Rから始まる人:r人、Cから始まる人:c人、Hから始まる人:h人
# 例えばM、A、Rから始まる人達から3人選ぶ方法:m * a * r通り
n = gets.to_i
s = Hash.new(0)
# 先頭文字をカウント
n.times { s[gets.chomp[0]] += 1 }
cnt = 0
# M,A,R,C,Hから3つを重複無しで配列化
["M", "A", "R", "C", "H"].combination(3).each { |i|
  # 重複無しパターンでそれぞれ3人の組み合わせを出す
  cnt += s[i[0]] * s[i[1]] * s[i[2]]
}
puts cnt
```
