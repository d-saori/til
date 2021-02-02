- A問題（https://atcoder.jp/contests/abc181/tasks/abc181_a）

```
n = gets.chomp.to_i
 
if n % 2 == 0
  puts "White"
else
  puts "Black"
end
```

- B問題（https://atcoder.jp/contests/abc181/tasks/abc181_b）
 - 整数の和：https://mathwords.net/1karannowa

```
# TLEで不正解だったコード
n = gets.to_i
num = []
n.times {
  a, b = gets.split.map(&:to_i)
  num << [*a..b]
}
puts num.flatten.sum

# 別解
n = gets.to_i
sum = 0
n.times {
  a, b = gets.split.map(&:to_i)
  sum += (a..b).sum
}
puts sum

# 黒板に書かれている整数は最大で10**11個になるため、黒板に書かれている整数を1つずつ足して行くとTLEになってしまうので、まとめて足す
# 1以上x以下の全ての整数の和=x*(x+1)/2
# (A以上B以下の全ての整数の和)=(1以上B以下の全ての整数の和)-(1以上A-1以下の全ての整数の和)=B*(B+1)/2-A*(A-1)/2
n = gets.to_i
sum = 0
n.times {
  a, b = gets.split.map(&:to_i)
  sum += b * (b + 1) / 2 - a * (a + 1) / 2  #=> sum += (a + b) * (b - a + 1) / 2
}
puts sum
```
