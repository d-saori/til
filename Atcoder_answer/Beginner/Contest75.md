- A問題（https://atcoder.jp/contests/abc075/tasks/abc075_a）
```
ary = gets.split.map(&:to_i)
puts ary.min_by { |v| ary.count(v) }

もしくは
ary = gets.split.map(&:to_i)
puts ary.select { |v| ary.count(v) == 1 }
```

- B問題（https://atcoder.jp/contests/abc075/tasks/abc075_b）
```
h, w = gets.split.map(&:to_i)
s = h.times.map{gets.chomp.to_s}
# [y, x]として8方向(マス右側から反時計回り)
b = [[0, 1], [1, 1], [1, 0], [1, -1], [0, -1], [-1, -1], [-1, 0], [-1, 1]]

h.times { |i|
  w.times { |j|
    if s[i][j] == "."
      sum = 0
      b.each { |y, x|
        ny = i + y
        nx = j + x 
        if 0 <= ny && ny < h && 0 <= nx && nx < w
          if s[ny][nx] == "#"
            sum += 1
          end
        end
      }
      s[i][j] = sum.to_s
    end
  }
}
s.each { |t| puts t}
```
