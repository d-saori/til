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
