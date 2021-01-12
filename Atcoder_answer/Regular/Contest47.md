- A問題
```
n, l = gets.split.map(&:to_i)
s = gets.chomp.chars
p = 1
ans = 0
s.each { |i|
  if i == "+"
    p += 1
    if p > l
      ans += 1
      p = 1
    end
  else
    p -= 1
  end
}
puts ans
```
