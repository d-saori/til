- A問題
```
n = gets.to_i
cnt = 0
(1..n-1).each { |i|
  (1..n-1).each { |j|
    cnt += 1 if i + j == n
  }
}
puts cnt

# 別解
n = gets.to_i
# A君とB君のお菓子の個数の和はn個になるので、片方が確定すればもう片方が確定する
# 片方、仮にA君のお菓子の個数の組み合わせを考える
# 1個以上のお菓子を得る必要があるので1以上であるが、n個全てを得るとB君が0個になってしまうので最大はn-1個
# お菓子は1〜n-1なのでn-1通り
puts n - 1
```

- B問題
```
n = gets.chomp
a = n.to_i(10).to_s
b = a.chars.reverse
cnt = 0
b.each { |i|
  cnt += 1 if i == "0"
}
if a == a.reverse
  puts "Yes"
else
  c = "0" * cnt + a
  puts c == c.reverse ? "Yes" : "No"
end

# 別解
# n <= 10 ** 9 なので0が0〜9個までそれぞれの場合について回文になるか判定
n = gets.chomp
(0..9).each { |i|
  a = "0" * i + n
  if a == a.reverse
    puts "Yes"
    exit
  end
}
puts "No"

# 別解
# 0を除いた文字列が回文でなければ0を足しても成り立たない
n = gets.chomp
n.sub!(/0*$/, "")
puts n == n.reverse ? "Yes" : "No"
```
