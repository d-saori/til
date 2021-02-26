- A問題
```
x, y = gets.split.map(&:to_i)
a = [1, 3, 5, 7, 8, 10, 12]
b = [4, 6, 9, 11]
c = [2]
puts a.include?(x) && a.include?(y) || b.include?(x) && b.include?(y) || c.include?(x) && c.include?(c) ? "Yes" : "No"
```

- B問題
```
h, w = gets.split.map(&:to_i)
puts "#" * (w + 2)
h.times { print "#", gets.chomp, "#\n" }
puts "#" * (w + 2)

# 別解
h, w = gets.split.map(&:to_i)
puts "#" * (w + 2)
h.times {
  puts "##{gets.chomp}#"
}
puts "#" * (w + 2)
```
