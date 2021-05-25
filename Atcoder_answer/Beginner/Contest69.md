- A問題（https://atcoder.jp/contests/abc069/tasks/abc069_a）
```
n, m = gets.split.map(&:to_i)
# 
puts (n - 1) * (m - 1)
```

- B問題（https://atcoder.jp/contests/abc069/tasks/abc069_b）
```
# 自分の解答
s = gets.chomp
puts "#{s[0]}#{s[1..-2].size}#{s[-1]}"

# 別解
s = gets.chomp
# s.length - 2：全体の文字数から先頭と末尾の2文字数を引く
puts s[0] + (s.length - 2).to_s + s[-1]
```

- C問題
```
n = gets.to_i
a = gets.split.map(&:to_i)
b = 0
c = 0
a.each { |i|
  if i % 4 == 0
    c += 1
  elsif i % 2 == 0
    b += 1
  end
}
puts c + b / 2 >= n / 2 ? "Yes" : "No"
```
