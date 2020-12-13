- A問題（https://atcoder.jp/contests/abc071/tasks/abc071_a）
```
x, a, b = gets.split.map(&:to_i)
if (b - x).abs > (a - x).abs
  puts "A"
else
  puts "B"
end
```

- B問題（https://atcoder.jp/contests/abc071/tasks/abc071_b）
```
s = gets.chomp.split("").sort.uniq.join
ans = "None"
("a".."z").each { |num|
  # unless文:条件式が偽になった場合(ブロック引数|num|が配列sに含まれていない時)に処理を実行
  unless s.include?(num)
    ans = num
    break
  end
}
puts ans
```
