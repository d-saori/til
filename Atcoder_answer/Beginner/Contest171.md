- A問題（https://atcoder.jp/contests/abc171）

```
input = gets.chomp
if a == a.upcase
  puts "A"
else
  puts "a"
end
と回答したが、正規表現を使用してのコードも利用できる。

# match?メソッド：=~やmatchメソッドよりも高速に動作
# \A：文字列の先頭
# \z：文字列の末尾
# [a-z]+：英小文字を少なくとも1文字以上繰り返す
# [A-Z]+：英大文字を少なくとも1文字以上繰り返す
input = gets.chomp
puts "a" if input.match?(/\A[a-z]+\z/)
puts "A" if input.match?(/\A[A-Z]+\z/)
```
