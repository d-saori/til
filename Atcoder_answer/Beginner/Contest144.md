- A問題（https://atcoder.jp/contests/abc144/tasks/abc144_a）

```
a, b = gets.split.map(&:to_i)

if a < 10 && b < 10
  puts a * b
else
  puts -1
end
```

- B問題（https://atcoder.jp/contests/abc144/tasks/abc144_b）
```
# N = A * B となるような 1 以上 9 以下の整数 A, B が存在するかどうか全探索で確かめる
n = gets.to_i
ans = "No"
(1..9).each { |i|
  (1..9).each { |j|
  if i * j == n
    ans = "Yes"
    break
  end
  }
}
puts ans
```
