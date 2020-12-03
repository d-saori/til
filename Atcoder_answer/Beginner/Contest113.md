- A問題（https://atcoder.jp/contests/abc113/tasks/abc113_a）

```
x, y = gets.split.map(&:to_i)

puts x + (y / 2)
```

- B問題（https://atcoder.jp/contests/abc113/tasks/abc113_b）
```
n = gets.to_i
t, a = gets.split.map(&:to_i)
h = gets.split.map(&:to_i)

# min_byメソッド:各要素を順番にブロックに渡して評価し、その評価結果を <=> で比較して、最小であった値に対応する元の要素、もしくは最小の n 要素を返す
num = h.min_by { |i| ((t - i * 0.006) - a).abs }
puts h.index(num) + 1

もしくは
n = gets.to_i
t, a = gets.split.map(&:to_i)
h = gets.split.map(&:to_i)

puts (1..n).min_by { |x| (a - t + h[x - 1] * 0.006).abs }
```
