- A問題（https://atcoder.jp/contests/abc075/tasks/abc075_a）
```
ary = gets.split.map(&:to_i)
puts ary.min_by { |v| ary.count(v) }

もしくは
ary = gets.split.map(&:to_i)
puts ary.select { |v| ary.count(v) == 1 }
```
