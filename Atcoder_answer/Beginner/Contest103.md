- A問題（https://atcoder.jp/contests/abc103/tasks/abc103_a）

```
# Aiの小さいタスクから順に、またはAiの大きいタスクから順に完了したときに最小となり、A1, A2, A3 の最大値と最小値の差が答えになる
a, b, c = gets.split.map(&:to_i).sort
puts c - a

または
a = gets.split.map(&:to_i).sort
puts a[2] - a[0]

または
a = gets.split.map(&:to_i)
puts a.max - a.min
```
