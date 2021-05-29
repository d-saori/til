- A問題
```
abc = gets.split.map(&:to_i).sort
puts abc[0] + abc[1]

# 別解
abc = gets.split.map(&:to_i).sort
# [0, 2]：インデックス番号0の要素から2つ選択
puts abc[0, 2].sum
```

- B問題
```
s = gets.chomp
# 文字列の前半と後半が全く同じであれば偶文字列
# 偶文字列の長さは必ず偶数長なので、偶数の文字列についてのみ調べる
# s.size - 2, s.size - 4...という順に調べて条件に合うものが見つかった時それを出力する
(s.size - 2).downto(2) { |i|
  next if i.odd?
  if s[0...i/2] == s[i/2...i]
    puts i
    break
  end
}

# 別解
s = gets.chomp
(s.length - 2).step(2, -2) { |i|
  if (0..(i / 2 -1)).all? { |j| s[j] == s[i / 2 + j] }
    puts i
    exit
  end
}
```

- C問題
```
n = gets.to_i
a = gets.split.map(&:to_i)
b = []
n.times { |i|
  i.even? ? b << a[i] : b.unshift(a[i])
}
puts (n.odd? ? b.reverse : b).join(" ")
```
