- A問題（https://atcoder.jp/contests/abc069/tasks/abc069_a）
```
n, m = gets.split.map(&:to_i)
# 
puts (n - 1) * (m - 1)
```

- B問題（https://atcoder.jp/contests/abc069/tasks/abc069_b）
```
# 自分の解答
s = gets.chomp.split("")
a = s[1..-2].count
puts "#{s[0]}#{a}#{s[-1]}"

# 別解
s = gets.chomp
# s.length - 2：全体の文字数から先頭と末尾の2文字数を引く
puts s[0] + (s.length - 2).to_s + s[-1]
```
