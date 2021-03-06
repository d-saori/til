- A問題（https://atcoder.jp/contests/abc185/tasks/abc185_a）
```
a = gets.chomp.split.map(&:to_i)
puts a.min
```

- B問題（https://atcoder.jp/contests/abc185/tasks/abc185_a）
```
n, m, t = gets.split.map(&:to_i)
ab = m.times.map{gets.split.map(&:to_i)}
s = n - ab[0][0] # 1件目のカフェ到着時の残りバッテリー量
g = t - ab[-1][1] # 最後に滞在したカフェを出発してから帰宅までに消費したバッテリー量
if s <= 0
  puts "No"
else
  m.times { |i|
    s = s + ab[i][1] - ab[i][0]
    if s >= n
      s = n
    end

    if m - 1 == i
      break
    else
      s = s - ab[i+1][0] + ab[i][1]
      if s <= 0
        break
      end
    end
  }
  if s - g > 0 ? "Yes" : "No"
end

# 別解
n, m, t = gets.split.map(&:to_i)
battery = n  #バッテリー総量
prev = 0
ans = "Yes"
m.times {
  a, b = gets.split.map(&:to_i)
  charge = b - a
  battery -= a - prev
  break ans = "No" if battery <= 0
  battery = [battery + b - a, n].min
  prev = b
}
puts battery - t + prev <= 0 ? "No" : ans
```
