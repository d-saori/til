- A問題（https://atcoder.jp/contests/arc106/tasks/arc106_a）

```
n = gets.to_i
# 3 ** 38 > 10 ** 18
# 5 ** 26 > 10 ** 18
cnt = 0
(0..38).each { |a|
  (0..26).each { |b|
    if 3 ** a + 5 ** b == n
      cnt += 1
      puts [a, b].join(" ")
      exit
    end
  }
}
puts -1
```
