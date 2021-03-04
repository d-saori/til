- A問題
```
s, e = gets.split.map(&:to_i)
ss, f = gets.split.map(&:to_i)
sss, g = gets.split.map(&:to_i)

se_sum = s * e.to_f / 10
ssf_sum = ss * f.to_f / 10
sssg_sum = sss * g.to_f / 10

puts se_sum.to_i + ssf_sum.to_i + sssg_sum.to_i

# 別解1
sum = 0
3.times {
  sum += gets.split.map(&:to_i).inject(:*) / 10
}
puts sum

# 別解2
sum = 0
3.times {
  s, e = gets.split.map(&:to_i)
  sum += s / 10 * e
}
puts sum
```

- B問題
```
x = gets.chomp.gsub(/ch/, "").gsub(/o/, "").gsub(/k/, "").gsub(/u/, "")
puts x.empty? ? "YES" : "NO"
```
