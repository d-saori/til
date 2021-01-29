- A問題（https://atcoder.jp/contests/abc071/tasks/abc071_a）
```
s = gets.chomp.chars
puts s.count("1")
```

- B問題（https://atcoder.jp/contests/abc071/tasks/abc071_b）
```
n = gets.to_i
a = gets.split.map(&:to_i)
cnt = 0
while a.all?(&:even?)
  a = a.map { |i| i / 2 }
  cnt += 1
end
puts cnt
```

- C問題（https://atcoder.jp/contests/abc081/tasks/arc086_a）
```
#  「できるだけ少ない数のボールの整数を書き換える」=「できるだけ多くのボールの整数を，変更しないままにしておく」=ハッシュのバリューが少ないもの
まにしておく」と
n, k = gets.split.map(&:to_i)
a = gets.split.map(&:to_i)
if a.uniq.size <= k
  puts 0
else
  b = a.group_by(&:itself).values.map(&:size).sort
  # [start, length]:[0, 2]=インデックス番号0と1の計2
  puts b[0, b.size - k].sum
end
```
