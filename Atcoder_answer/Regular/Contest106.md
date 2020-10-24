- A問題（https://atcoder.jp/contests/arc106/tasks/arc106_a）

```
n = gets.to_i
# 3 ** x <= 10 ** 18 →30 ** 37
(1..37).each do |a|
  (1..37).each do |b|
    if 3**a + 5**b == n
      puts "#{a} #{b}"
      exit
    end
  end
end

puts "-1"
```
