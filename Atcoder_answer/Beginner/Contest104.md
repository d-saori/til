- A問題（https://atcoder.jp/contests/abc104/tasks/abc104_a）

```
r = gets.to_i

if r < 1200
  puts "ABC"
elsif r < 2800
  puts "ARC"
else
  puts "AGC"
end
```

- B問題
```
s = gets.chomp
puts s.start_with?("A") && s[2..-2].scan("C").size == 1 && s.delete("AC") == s.delete("AC").downcase ? "AC" : "WA"

# 別解
s = gets.chomp
puts s.match(/^A[a_z]+C[a_z]+$/) ? "AC" : "WA"
```
