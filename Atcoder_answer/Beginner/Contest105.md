- A問題（https://atcoder.jp/contests/abc105/tasks/abc105_a）

```
n, k = gets.split.map(&:to_i)
puts n % k == 0 ? 0 : 1
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

# 別解
n = gets.to_i
sum = []
(0..n/4).each { |i|
  (0..n/7).each { |j|
    sum << i * 4 + j * 7
  }
}
puts sum.include?(n) ? "Yes" : "No"
```
