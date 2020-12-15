- A問題（https://atcoder.jp/contests/abc047/tasks/abc047_a）
```
abc = gets.split.map(&:to_i).sort
puts abc[0] + abc[1] == abc[2] ? "Yes" : "No"
```

- B問題（https://atcoder.jp/contests/abc047/tasks/abc047_b）
```
w, h, n = gets.split.map(&:to_i)

x_min = 0
x_max = w
y_min = 0
y_max = h

n.times {
  x, y, a = gets.split.map(&:to_i)
    if a == 1
      x_min = x if x > x_min
    elsif a == 2
      x_max = x if x < x_max
    elsif a == 3
      y_min = y if y > y_min
    else
      y_max = y if y < y_max
    end
}
if x_max - x_min > 0 && y_max - y_min > 0
  puts (x_max - x_min) * (y_max - y_min)
else
  puts 0
end
```
