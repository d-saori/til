- A問題
```
# 順位 = (その人より多くの得点を獲得した人数)+1
abc = 3.times.map { gets.to_i }
ss = abc.sort.reverse
abc.each { |i|
  puts ss.index(i) + 1
}
```
