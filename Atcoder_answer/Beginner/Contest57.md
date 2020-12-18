- A問題（https://atcoder.jp/contests/abc057/tasks/abc057_a）
```
a, b = gets.split.map(&:to_i)
# if a + b >= 24
#   puts (a + b) - 24
# else
#   puts a + b
# end
puts a + b >= 24 ? (a + b) - 24 : a + b
```

- B問題（https://atcoder.jp/contests/abc057/tasks/abc057_b）
```
n, m = gets.split.map(&:to_i)
students = n.times.map{gets.split.map(&:to_i)}
checkpoints = m.times.map{gets.split.map(&:to_i)}

students.each { |a, b|
  d = checkpoints.map{ |c, d| (a - c).abs + (b - d).abs }
  puts d.index(d.min) + 1
}
```

- C問題（https://atcoder.jp/contests/abc057/tasks/abc057_c）
```
n = gets.to_i
# n = A * Bを満たす2つの整数は共にnの約数。
# 交換法則n = A * B = B * AからA ≤ Bを満たすAを列挙すればいい。、
x = (n ** 0.5).floor
f = 1

# 整数nの桁数は以下の2つで求められる
# 整数nを10進表記の文字列に変換した時の文字列の長さ
# 整数nを0になるまで10で繰り返し割った時の回数
(1..x).each { |i|
  if n % i == 0
    f = (n / i).to_s.size
  end
}
puts f
```
