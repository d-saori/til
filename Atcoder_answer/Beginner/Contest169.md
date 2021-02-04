- A問題（https://atcoder.jp/contests/abc169/tasks/abc169_a）

```
A, B = gets.split(" ").map(&:to_i)
puts A * B
```

- B問題
```
# そのまま探索するとTLEになってしまうので工夫する
n = gets.to_i
a = gets.split.map(&:to_i).sort
sum = 1
a.each { |i|
  sum *= i
  if sum > 10 ** 18
    puts -1
    exit
  end
}
puts sum

# 別解
n = gets.to_i
a = gets.split.map(&:to_i)
sum = 1
if a.include?(0)
  puts 0
else
  a.each { |i|
    sum *= i
    if sum > 10 ** 18
      puts -1
      exit
    end
  }
  puts sum
end
```
