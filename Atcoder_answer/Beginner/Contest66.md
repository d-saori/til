- A問題
```
abc = gets.split.map(&:to_i).sort
puts abc[0] + abc[1]

# 別解
abc = gets.split.map(&:to_i).sort
# [0, 2]：インデックス番号0の要素から2つ選択
puts abc[0, 2].sum
```
