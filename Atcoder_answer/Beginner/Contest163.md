- A問題（https://atcoder.jp/contests/abc163/tasks/abc163_a）

```
r = gets.to_f
puts 2 * r * 3.14

# 円周率は、Math::PI (=> 3.141592654)とも書ける
r = gets.to_f
puts 2 * r * Math::PI
```

- B問題
```
n, m = gets.split.map(&:to_i)
a = gets.split.map(&:to_i)
puts n - a.sum >= 0 ? n - a.sum : -1
```

- C問題
```
n = gets.to_i
a = gets.split.map(&:to_i)
ans = [0] * (n + 1)
a.each { |i|
  ans[i] += 1
}
ans.shift
puts ans
```
