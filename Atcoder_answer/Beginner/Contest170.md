- A問題（https://atcoder.jp/contests/abc170/tasks/abc170_a）

```
x = gets.split.map(&:to_i)

# splitメソッドは文字列を配列に分割するメソッド。インデックス番号(ここではxiの事)は0から始まるので、+1が必要
x.each_with_index do |num, xi|
  if num == 0
    puts xi + 1
  end
end

# 別解答
x = gets.split.map(&:to_i)
puts x.index(0) + 1
```

