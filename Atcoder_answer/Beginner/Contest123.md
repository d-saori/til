- A問題（https://atcoder.jp/contests/abc123/tasks/abc123_a）

```
a = gets.to_i
b = gets.to_i
c = gets.to_i
d = gets.to_i
e = gets.to_i
k = gets.to_i
# a,b,c,d,e,k = 6.times.map{gets.to_i} とも書ける

if e - a > k
  puts ":("
else 
  puts "Yay!"
end
```

- B問題
```
# 最後に注文した方が良さそうな料理を決める
# 注文してから次の注文までの時刻は10の倍数
# 調理時間x分の料理について、注文してから次の注文までの時刻は「x以上の最小の10の倍数分」
# 最後に注文する料理以外は「x以上の最小の10の倍数分」かかるとみなして良い
# 最後に注文する料理は、調理時間そのままの時間がかかるので「(x以上の最小の10の倍数)とxの差」が最大になる料理を選ぶ
a = 5.times.map { gets.to_i }
m = a.map { |x| x % 10 }.map { |x| x == 0 ? 10 : x }.min
puts a.map { |x| (x + 9) / 10 * 10 }.sum - 10 + m

# 別解
a = 5.times.map { gets.to_i }
b = a.map { |i| (i % 10) == 0 ? 0 : 10 - (i % 10) }
puts a.sum + b.sum - b.max
```

- C問題
```
n = gets.to_i
a = 5.times.map { gets.to_f }.min
puts (n / a).ceil + 4
```
