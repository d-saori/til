- A問題（https://atcoder.jp/contests/abc099/tasks/abc099_a）

```
n = gets.to_i
if n <= 999
  puts "ABC"
else
  puts "ABD"
end
```

- B問題
```
a, b = gets.split.map(&:to_i)
# 高さ(1+2+3+..+x)mの塔から、西に1mの地点にある塔の高さは(1+2+3+..+x-1)
# 上記より2本の塔の高さの差は、x
# 雪の埋もれていない部分の高さがbの塔の高さ:(1+2+3+..+b-a)
# (1+2+3+..+x)=x*(x+1)/2
puts (b - a) * (b - a + 1) / 2 - b

# 別解
a, b = gets.split.map(&:to_i)
# 高さ(1+2+3+..+x)mの塔から、西に1mの地点にある塔の高さは(1+2+3+..+x-1)
# 上記より2本の塔の高さの差は、x:b-a
# bの塔全体の高さ:(1+2+3+..+b-a)から雪に埋もれていない部分を引けば、積もった雪の高さがでる
puts [*1..(b-a)].sum - b

# 別解
a, b = gets.split.map(&:to_i)
m = b - a
b_sum = 0
[*1..m].each { |i| b_sum += i }
puts b_sum - b
```
