- A問題（https://atcoder.jp/contests/arc109/tasks/arc109_a)
```
# 自分の解答（Aｌｌの内1つ不正解だった）
a, b, x, y = gets.split.map(&:to_i)
# aがbより1階高い、aとbが同じ階の時は廊下が繋がっているので最短距離は廊下を渡れば良い
if a - b == 1 || a == b
  puts x
# aがbより1階以上高い場合。
elsif a > b
# b階まで階段を降り廊下を渡る：(a - b) * y + x
# b+1階まで階段を降り廊下を渡る：(a - (b + 1)) * y + x
  puts [(a - b) * y + x, (a - (b + 1)) * y + x].min
# それ以外（b > a）
else
# b階まで階段を登り廊下を渡る：(b - a) * y + x
# ai階からbi階に廊下を渡り、biからai+1階に廊下を渡るのをb-a回繰り返し、最後に目標のb階へ廊下を渡る：(b - a) * (2 * x) + x
  puts [(b - a) * y + x, (b - a) * (2 * x) + x].min
end

a, b, x, y = gets.split.map(&:to_i)
if a - b == 1 || a == b
  puts x
elsif a > b
# aがb+1階まで降りて、廊下を渡ってbに渡る：(a - b - 1) * y + x
# aからb-1に廊下を渡って降り、b-1からaiに渡りを繰り返し、最後にaがbと同じ階まで降りので+x：(a - b - 1) * (2 * x) + x
  puts [(a - b - 1) * y + x, (a - b - 1) * (2 * x) + x].min
else
  puts [(b - a) * y + x, (b - a) * (2 * x) + x].min
end
```
