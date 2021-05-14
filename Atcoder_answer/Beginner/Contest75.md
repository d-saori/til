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
s = h.times.map{gets.chomp}
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

# 別解
h, w = gets.split.map(&:to_i)
s = h.times.map { gets.chomp.chars }
h.times { |i|
  w.times { |j|
    if s[h][w] != "#"
      s[h][w] = s[[0, h - 1].max..h + 1].flat_map { |t| t[[0, w - 1].max..w + 1] }.count("#")
    end
  }
}
puts s.map(&:join)

# 別解
h, w = gets.split.map(&:to_i)
s = h.times.map { gets.chomp.chars }
dy = [-1, -1, 0, 1, 1, 1, 0, -1]
dx = [0, 1, 1, 1, 0, -1, -1, -1]
h.times { |y|
  w.times { |x|
    print s[y][x] == "#" ? "#" : (0..7).count { |i|
      a, b = y + dy[i], x + dx[i]
      0 <= a && a < h && 0 <= b && b < w && s[a][b] == "#"
    }
  }
  puts ""
}

# 別解
h, w = gets.split.map(&:to_i)
s = h.times.map { gets.chomp.chars }
dx = [1, 1, 1, 0, 0, -1, -1, -1]
dy = [1, 0, -1, 1, -1, 1, -1, 0]

h.times { |x|
  w.times { |y|
    cnt = 0
    8.times { |k|
      cnt += 1 if x + dx[k] >= 0 && x + dx[k] < h && y + dy[k] >= 0 && y + dy[k] < w && s[x + dx[k]][y + dy[k]] == "#"
    }
    print "#" if s[x][y] == "#"
    print cnt if s[x][y] != "#"
  }
  puts
}
```
