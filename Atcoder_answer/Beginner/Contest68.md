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

- C問題
```
# 島1と島i、島iと島nのどちらの間にも定期便が通っているようなiが存在するかどうかを調べる
n, m = gets.split.map(&:to_i)
all = []
check_first = []
check_last = []
m.times {
  v = gets.split.map(&:to_i)
  if v[0] == 1
    check_first << v[1]
  elsif v[1] == n
    check_last << v[0]
  end
}
puts (check_first & check_last)[0] != nil ? "POSSIBLE" : "IMPOSSIBLE"
```
