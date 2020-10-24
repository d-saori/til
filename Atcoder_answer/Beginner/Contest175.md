- A問題（https://atcoder.jp/contests/abc175/tasks/abc175_a）
  - 天気の組合せは、1,2,3日目がそれぞれ晴れ、雨かどうかで2**3=8通りしかないので、8通りの場合分けを書けば正答することができる。


```
S = gets.chomp

if S == "RRR"
  puts 3
elsif S == "SSS"
  puts 0
elsif S == "SSR" or S == "RRS"
  puts 2
else
  puts 1
end
```

<br>

```
# その他の回答
# coding: utf-8
# R+でRに合致する最大のRをarrayに格納して返す。そこからもっとも長いRの長さを取得して、||0でnilガード。そこからsizeをとる
p (gets.scan(/R+/).max || "").size
```
