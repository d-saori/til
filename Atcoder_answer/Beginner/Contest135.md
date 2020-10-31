- A問題（https://atcoder.jp/contests/abc135/tasks/abc135_a）

```
# AとBの偶奇が異なるとき、どのような整数Kについても |A − K| と |B − K| の偶奇は異なるので、答えはIMPOSSIBLE
# AとBの偶奇が等しいとき、K=A+B/2 とおくと Kは整数。また |A − K| = |(A−B)/2|, |B − K| = |(B−A)/2| となり、絶対値の定義より両者は等しいことが言える。

a, b = gets.split.map(&:to_i)

if (a + b) % 2 == 0
  puts (a + b) / 2
else
  puts "IMPOSSIBLE"
end
```
