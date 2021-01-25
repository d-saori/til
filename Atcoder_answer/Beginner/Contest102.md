- A問題（https://atcoder.jp/contests/abc102/tasks/abc102_a）

```
# lcmメソッド:最小公倍数を得る
n = gets.to_i
# puts 2.lcm(n)
puts n.lcm(2)
```

- B問題
```
# 自分の回答
n = gets.to_i
a = gets.split.map(&:to_i)
b = []
a.each { |i|
  a.each { |j|
    b << (i - j).abs
  }
}
puts b.max

# 別解
n = gets.to_i
a = gets.split.map(&:to_i)
puts a.max - a.min
```
