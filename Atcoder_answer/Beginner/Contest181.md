- A問題（https://atcoder.jp/contests/abc181/tasks/abc181_a）

```
n = gets.chomp.to_i
 
if n % 2 == 0
  puts "White"
else
  puts "Black"
end
```

- B問題（https://atcoder.jp/contests/abc181/tasks/abc181_b）
 - 整数の和：https://mathwords.net/1karannowa

```
n = gets.to_i
ans = 0
for i in (1..n)
    a,b = gets.split(" ").map(&:to_i)
    ans += b * (b + 1) / 2 - a * (a - 1) / 2
end
p ans

もしくは

n = gets.chomp.to_i
sum = 0

n.times.map{
	a, b = gets.split.map(&:to_i)
	sum += (a+b)*(b-a+1)/2
}

puts sum
```
