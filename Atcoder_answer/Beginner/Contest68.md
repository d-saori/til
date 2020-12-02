- A問題（https://atcoder.jp/contests/abc068/tasks/abc068_a）
```
n = gets
puts "ABC#{n}"

もしくは
puts "ABC"+gets
```

- B問題（https://atcoder.jp/contests/abc068/tasks/abc068_b）
```
# 2 で k 回割れる数のうち最も小さいものは 2 を k 回かけた数：100 以下だと1, 2, 4, 8, 16, 32, 64の 7 種類なので　この中から　N 以下で最も大きいものを出力する
n = gets.to_i
arr = [1, 2, 4, 8, 16, 32, 64]
if n == 1
  puts n
else
  count = 0
  arr.each do |num|
    if num <= n
      count = num
    end
  end
  puts count
end

もしくは
n = gets.to_i
[64, 32, 16, 8, 4, 2, 1].each { |i|
    if i <= n
        puts i
        break
    end
}
```
