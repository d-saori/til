- A問題(https://atcoder.jp/contests/abc179/tasks/abc179_a)

```
# 自分の回答
S = gets.to_s

if /S$/ == "e"
  puts "S" + "es"
else
  puts "S" + "s"
end
なぜか正規表現を使って一致させようと考えていた…
```

- 「入力された文字列の最後の1文字」を見て条件分岐する必要がある。
- 「文字列のi番目の文字」を得る方法を使う。

```
S = gets.chomp

if S[-1] == "s"
  puts "#{S}" + "es"
else
  puts "#{S}" + "s"
end
```