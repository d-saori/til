- A問題
```
# 順位 = (その人より多くの得点を獲得した人数)+1
abc = 3.times.map { gets.to_i }
ss = abc.sort.reverse
abc.each { |i|
  puts ss.index(i) + 1
}

# 別解
a = gets.to_i
b = gets.to_i
c = gets.to_i
abc = [a, b, c].sort.reverse
puts abc.index(a) + 1
puts abc.index(b) + 1
puts abc.index(c) + 1
```
