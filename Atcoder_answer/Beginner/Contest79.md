- A問題
```
n = gets.chomp.chars
puts n[0..2].uniq.size == 1 || n[1..3].uniq.size == 1 || n.uniq.size == 1 ? "Yes" : "No"

# 別解
n = gets.chomp.chars.sort
puts n.count(n[1]) >= 3 ? "Yes" : "No"
```

- B問題
```
n = gets.to_i
ary = [2, 1]
n.times {
  ary << ary[-2] + ary[-1]
}
puts ary[n]
```

- C問題
```
a, b, c, d = gets.chomp.chars
["+", "-"].repeated_permutation(3) { |op1, op2, op3|
  e = a + op1 + b + op2 + c + op3 + d
  # eval("puts 'e'")
  if eval(e) == 7
    puts "#{e}=7"
    exit
  end
}
```
