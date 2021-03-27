- A問題（https://atcoder.jp/contests/abc136/tasks/abc136_a）

```
a, b, c = gets.split.map(&:to_i)
puts b + c < a ? 0 : c - (a - b)

# 別解
a, b, c = gets.split.map(&:to_i)
puts [c - a + b, 0].max
```

- B問題（https://atcoder.jp/contests/abc136/tasks/abc136_b）
```
n = gets.to_i
cnt = 0
(1..n).each { |i|
  if i.to_s.size % 2 != 0
  cnt += 1
  end
}
puts cnt

# 別解
n = gets.to_i
sum = 0
[*1..n].each { |i|
  if i.to_s.size.odd?
  sum += 1
  end
}
puts sum
```

- C問題
```
n = gets.to_i
h = gets.split.map(&:to_i)
max = 0
(1..n-1).each { |i|
  if h[i] < max - 1
    puts "No"
    exit
  end
  max = [max, h[i]].max
}
puts "Yes"

# 別解
n = gets.to_i
h = gets.split.map(&:to_i)
max = h[-1]
flag = true
h.reverse.each { |i|
  if i <= max
    max = i
  else
    if i - 1 == max
      next
    else
      flag = false
      break
    end
  end
}
puts flag ? "Yes" : "No"
```
