- A問題（https://atcoder.jp/contests/abc119/tasks/abc119_a）

```
s = gets.chomp
puts s <= "2019/04/30" ? "Heisei" : "TBD"
```

- B問題
```
n = gets.to_i
oto = []
n.times {
  x, u = gets.chomp.split
  if u == "JPY"
    oto << x.to_i
  else
    oto << x.to_f * 380000
  end
}
puts oto.sum

# 別解
n = gets.to_i
sum = 0
n.times {
  x, u = gets.chomp.split
  sum += x.to_f * (u == "JPY" ? 1 : 380000)
}
puts sum
```

- C問題
```
@n, @a, @b, @c = gets.split.map(&:to_i)
@l = @n.times.map { gets.to_i }
def dfs(i, a, b, c, cost)
  if i == @n
    return 10 ** 10 if a * b * c == 0
    # 最世の1つ目でもコスト10かかってしまっているので30を引く
    return (@a - a).abs + (@b - b).abs + (@c - c).abs + cost - 30
  end

  x = dfs(i + 1, a, b, c, cost)
  y = dfs(i + 1, a + @l[i], b, c, cost + 10)
  z = dfs(i + 1, a, b + @l[i], c, cost + 10)
  w = dfs(i + 1, a, b, c + @l[i], cost + 10)
  return [x, y, z, w].min
end
puts dfs(0, 0, 0, 0, 0)
```
