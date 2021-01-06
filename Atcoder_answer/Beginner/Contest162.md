- A問題（https://atcoder.jp/contests/abc162/tasks/abc162_a）

```
n = gets
puts n[0] == "7" || n[1] == "7" || n[2] == "7" ? "Yes" : "No"

# もしくは
n = gets
puts n.include?("7") ? "Yes" : "No"
```
