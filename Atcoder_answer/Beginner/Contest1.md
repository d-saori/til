- A問題
```
ha, hb = 2.times.map { gets.to_i }
puts ha - hb
```

- B問題
```
m = gets.to_i
if m <= 100
  puts 00
elsif 100 <= m && m <= 5000
  puts ("0" + m.to_s)[-4..-3]
elsif 6000 <= m && m <= 30000
  puts m / 1000 + 50
elsif 35 <= m && m <= 70
  puts (m - 30000) / 5000 + 80
else
  puts 89
end
```
