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

- B問題
```
x, y = gets.split.map(&:to_i)
cnt = 0
(0..x).each { |i|
  # 鶴がi匹なら亀はj = x - i匹
  cnt += 1 if i * 2 + (x - i) * 4 == y
}
puts cnt >= 1 ? "Yes" : "No"

# 別解
x, y = gets.split.map(&:to_i)
(0..x).each { |i|
  # 鶴がi匹なら亀はj = x - i匹
  if i * 2 + (x - i) * 4 == y
    puts "Yes"
  end
}
puts "No"
```

- C問題
```
x, n = gets.split.map(&:to_i)
p = gets.split.map(&:to_i)
ary = [*0..101] - p
puts ary.min_by { |i| (i - x).abs }
```
