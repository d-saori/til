- A問題（https://atcoder.jp/contests/abc185/tasks/abc185_a）
```
a = gets.chomp.split.map(&:to_i)
puts a.min
```

- B問題（https://atcoder.jp/contests/abc185/tasks/abc185_a）
```
n, m, t = gets.chomp.split.map(&:to_i)
ab = m.times.map{gets.split.map(&:to_i)} # [[a1, b1], [a2, b2]]...
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
  if s - g > 0
    puts "Yes"
  else
    puts "No"
  end
end

もしくは
n, m, t = gets.chomp.split.map(&:to_i)

prev = 0
spend = 0 #バッテリー消費量
battery = n #バッテリー総量
a, b = 0

m.times { |i|
  a, b = gets.chomp.split(" ").map(&:to_i)
  charge = b - a
  spend = a - prev # 1件目のカフェまでに消費したバッテリー量
  # まずここまでの消費を計算
  battery = battery - spend
  break if battery <= 0
  # カフェで充電した分を残バッテリー量に足す
  battery = battery + charge
  battery = n if battery > n
  prev = b
}

battery = battery - (t - b)
if battery > 0
  puts "Yes"
else
  puts "No"
end
```
