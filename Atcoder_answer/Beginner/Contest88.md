- A問題（https://atcoder.jp/contests/abc088/tasks/abc088_a）

```
# 𝑁 円を超えないようにできるだけ多くの 500 円硬貨を使うと 1 円硬貨の枚数は最小化される.
# 500 円硬貨は 「𝑁 を 500 で割ったときの商」 枚使われることになる。使用する 1 円硬貨の枚数は 𝑁 を 500 で割ったあまりになる。

# n = gets.to_i
# a = gets.to_i
n, a = 2.times.map{gets.to_i}

if n % 500 <= a
  puts "Yes"
else
  puts "No"
end
```

- B問題（https://atcoder.jp/contests/abc088/tasks/abc088_b）
```
n = gets.to_i
a = gets.split.map(&:to_i).sort.reverse
alice = a.each_slice(2).map(&:first).sum
bob = a.sum - alice
puts alice - bob
```

- C問題（https://atcoder.jp/contests/abc088/tasks/abc088_c）
```
ary = 3.times.map{gets.split.map(&:to_i)}

aa = [0, 0, 0]
bb = [0, 0, 0]
cnt = 0
(0..2).each { |i|
  (0..2).each { |j|
    aa[i] = ary[i][0] - bb[0]
    bb[j] = ary[0][j] - aa[0]
    cnt += 1 if ary[i][j] == aa[i] + bb[j]
  }
}
puts cnt == 9 ? "Yes" : "No"
```
