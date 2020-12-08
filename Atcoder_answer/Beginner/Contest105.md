- A問題（https://atcoder.jp/contests/abc105/tasks/abc105_a）

```
n, k = gets.split.map(&:to_i)

if n % k == 0
  puts 0
else
  puts 1
end
```

- B問題（https://atcoder.jp/contests/abc105/tasks/abc105_b）
```
n = gets.to_i
ans = "No"
(0..n/4).each { |i|
  (0..n/7).each { |j|
    if (4 * i + 7 * j) == n
      ans = "Yes"
      break
    end
  }
}
puts ans
```
