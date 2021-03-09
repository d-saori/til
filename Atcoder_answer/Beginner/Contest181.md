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

- C問題
```
n = gets.to_i
xy = n.times.map { gets.split.map(&:to_i) }
# 3点A(0, 0),B(x1, y1),C(x2, y2)が同一直線上にある条件:ABとACの傾きが等しい
# y1 / x1 = y2 / x2 :両辺にx1x2をかける: x2y1 = x1y2
xy.combination(3) { |a, b, c|
  x = b[0] - a[0]
  y = b[1] - a[1]
  if x == 0
    if c[0] == b[0]
      puts "Yes"
      exit
    end
  elsif y * (c[0] - a[0]) + x * a[1] == x * c[1]
    puts "Yes"
    exit
  end
}
puts "No"
```
