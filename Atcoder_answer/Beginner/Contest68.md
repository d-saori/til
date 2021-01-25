- A問題（https://atcoder.jp/contests/abc068/tasks/abc068_a）
```
n = gets
puts "ABC#{n}"

もしくは
puts "ABC"+gets
```

- B問題（https://atcoder.jp/contests/abc068/tasks/abc068_b）
```
n = gets.to_i
# 2をk回割れる数=2**k
# 100以下で上記を満たすのは:1,2,4,8,16,64
# この7種類のうちn以下で最も大きいものを出力すればOK
a = [1, 2, 4, 8, 16, 32, 64]
puts a.select { |i| i <= n }.max

# 別解
n = gets.to_i
[64, 32, 16, 8, 4, 2, 1].each { |i|
    if i <= n
        puts i
        break
    end
}
```
