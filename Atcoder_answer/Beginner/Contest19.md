- A問題
```
abc = gets.split.map(&:to_i).sort
puts abc[1]
```

- B問題
```
s = gets.chomp.chars
ary = []
f = s[0]
cnt = 0
a = 0
s.each { |i|
  if i != f
    ary << "#{f}#{cnt}"
    cnt = 1
    f = i
  else
    cnt += 1
  end
  if a == s.size - 1
    ary << "#{f}#{cnt}"
  end
  a += 1
}
puts ary.join("")

# 別解
s = gets.chomp
ans = ""
while s != ""
  i = 0
  while s[i] == s[0]
    i += 1
  end
  ans << (s[0] + "#{i}")
  s = s[i..-1]
end
puts ans
```
