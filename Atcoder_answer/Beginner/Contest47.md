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

# 別解
w, h, n = gets.split.map(&:to_i)
# 塗りつぶしていない長方形が存在した場合の左下座標(0, 0)、右上座標(w, h)
l, r, t, b = [0, w, h, 0]
n.times {
  x, y, a = gets.split.map(&:to_i)
  case(a)
  when 1
    l = [l, x].max
  when 2
    r = [r, x].min
  when 3
    b = [b, y].max
  when 4
    t = [t, y].min
  end
}
puts [r - l, 0].max * [t - b, 0].max
```
