- A問題（https://atcoder.jp/contests/abc047/tasks/abc047_a）
```
abc = gets.split.map(&:to_i).sort
puts abc[0] + abc[1] == abc[2] ? "Yes" : "No"
```

- B問題（https://atcoder.jp/contests/abc047/tasks/abc047_b）
```
w, h, n = gets.split.map(&:to_i)
x_min = 0
y_min = 0
n.times {
  x, y, a = gets.split.map(&:to_i)
  if a == 1
    x_min = [x_min, x].max
  elsif a == 2
    w = [w, x].min
  elsif a == 3
    y_min = [y_min, y].max
  else
    h = [h, y].min
  end
}
puts [w - x_min, 0].max * [h - y_min, 0].max
```
