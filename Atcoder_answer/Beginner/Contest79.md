- A問題
```
n = gets.chomp.chars
puts n[0..2].uniq.size == 1 || n[1..3].uniq.size == 1 || n.uniq.size == 1 ? "Yes" : "No"

# 別解
n = gets.chomp.chars.sort
puts n.count(n[1]) >= 3 ? "Yes" : "No"
```

- B問題
```
n = gets.to_i
ary = [2, 1]
n.times {
  ary << ary[-2] + ary[-1]
}
puts ary[n]
```
