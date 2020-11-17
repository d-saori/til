- PracticeA(https://atcoder.jp/contests/abs/tasks/practice_1)

```
a = gets.chomp.to_i
# スペース区切りの整数の入力
b, c = gets.chomp.split(" ").map(&:to_i)
s = gets.chomp

puts ("#{a + b + c} #{s}")
```

- Product(https://atcoder.jp/contests/abs/tasks/abc086_a)

```
# 自分の解答
a, b = gets.split(" ").map(&:to_i)
if a * b % 2 == 0
  puts "Even"
else
  puts "Odd"
end

# 他の書き方
a, b = gets.split(" ").map(&:to_i)
# odd?:奇数ならtrue
if (a * b).odd?
  puts "Odd"
else
  puts "Even"
end
```

- Placing Marble(https://atcoder.jp/contests/abs/tasks/abc081_a)

```
# 自分の解答（不正解）
a, b, c = gets.chomp.split.map(&:to_i)
if a == 1
  puts 1
elsif b == 0
  puts 0
elsif c == 1
  puts 1
else
  puts 0
end
puts a + b + c

# 解
ayy = gets.chomp
# charsメソッド：文字列中の1文字1文字を配列の要素に分解するメソッド
puts ayy.chars.count("1")

または
puts gets.chomp.count("1")
```

- Shift only
```
# 解
n = gets.chomp.to_i
nums = gets.split(" ").map(&:to_i)
count = 0

# 整数全てが偶数か判別する:all?メソッド（https://docs.ruby-lang.org/ja/latest/method/Enumerable/i/all=3f.html）
while nums.all? { |n| n.even} do
  nums.map! { |n| n / 2 }
  count += 1
end
puts count
```

- Coins(https://atcoder.jp/contests/abs/tasks/abc087_b)
```
# a = gets.to_i
# b = gets.to_i
# c = gets.to_i
# x = gets.to_i
a, b, c, x = 4.times.map{gets.to_i}

count = 0

(0..a).each do |i|
  if 500 * i <= x
    (0..b).each do |j|
      if 500 * i + 100 * j <= x
        (0..c).each do |k|
          if 500 * i + 100 * j + 50 * k == x
            count += 1
          end
        end
      end
    end
  end
end

puts count
```
