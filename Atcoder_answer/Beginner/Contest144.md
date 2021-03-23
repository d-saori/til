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

# 別解
n = gets.to_i
ans = 0
(1..9).each { |i|
  (1..9).each { |j|
    if i * j == n
      ans += 1
    end
  }
}
puts ans >= 1 ? "Yes" : "No"
```

- C問題
```
# (i, j) → i * j == n → 移動回数:i + j - 2
# (i, j).min <= √n <= 10**6
n = gets.to_i
i = Math.sqrt(n).to_i
(1..i).each { |a|
  if n % a == 0
    puts (a + (n / a) - 2)
    exit
  end
}
```
