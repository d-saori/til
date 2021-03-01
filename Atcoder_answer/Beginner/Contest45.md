- A問題
```
a, b, h = 3.times.map { gets.to_i }
puts (a + b) * h / 2
```

- B問題
```
cards = 3.times.map { gets.chomp }
turn = 0
index = [0, 0, 0]
card = nil
while card = cards[turn][index[turn]]
  nturn = "abc".index(card)
  index[turn] += 1
  turn = nturn
end
puts "ABC"[turn]
```
