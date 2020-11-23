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
# 多重each文で全探索
(0..a).each { |i|      # 500円玉が 0枚〜i枚 の場合 (i + 1 通り) を全て探索
  (0..b).each { |j|    # 100円玉が 0枚〜j枚 の場合 (j + 1 通り) を全て探索
    (0..c).each { |k|  # 50円玉が 0枚〜k枚 の場合 (k + 1 通り) を全て探索
      if x == (500 * i + 100 * j + 50 * k)
        count += 1
      else
        count += 0
      end
    }
  }
} 
puts count
```

- Some Sums(https://atcoder.jp/contests/abs/tasks/abc083_b)
```
n, a, b = gets.split(" ").map(&:to_i)
sum = 0
(1..n).each do |i|
  # この時点でiはsplitされた配列、splitは文字列に有効だからto_s
  x = i.to_s.split("").map(&:to_i).sum
  if x >= a && x <= b
    sum += i
  end
end
puts sum
```

- Card Game for Two(https://atcoder.jp/contests/abs/tasks/abc088_b)
```
n = gets.to_i
arr = gets.split(" ").map(&:to_i).sort.reverse # 数の大きい順に並べる
# 要素をインデックス番号、偶数番目と奇数番目とで分けたい。(https://qiita.com/ddd555/items/ed7db4b342b783620b41)を参考にする。
# Aliceはインデックス番号0と偶数の時のカード番号
a_arr = arr.each_slice(2).map(&:first)
# Bobは1から始まる奇数のインデックス番号
b_arr = arr.each_slice(2).map(&:last) 
p (a_arr.sum) - (b_arr.sum)

# nが奇数の時Bobのカード枚数が1枚多くなってしまう
# slice(2)で要素が1つの最後の配列をfirstとlastそれぞれでカウントしてしまってダメ

違う方法
n = gets.to_i
arr = gets.split(" ").map(&:to_i).sort.reverse # 数の大きい順に並べる
# インデックス番号が偶数の要素の合計(Aliceのカード合計)を求める
a_arr = arr.select.with_index { |e, i| i % 2 == 0 }.sum
# 配列全体の合計から↑の合計を引いて、インデックス番号が奇数の合計(Bobのカード合計)を求める
b_arr = arr.sum - a_arr
puts a_arr - b_arr
```

- Kagami Mochi（https://atcoder.jp/contests/abs/tasks/abc085_b）
```
n = gets.to_i
# 要素n個の配列ができる
a = n.times.map{gets.chomp.to_i}
# 配列aから重複した要素を取り除いた要素数（＝鏡餅の段数）を求める
p a.uniq.count
```

- Otoshidama(https://atcoder.jp/contests/abs/tasks/abc085_c)
```
n, y = gets.chomp.split(" ").map(&:to_i)

# 計算時間短縮の為、札の枚数3種類のうち2種類のみ探索する(2種類わかれば残りは総数nから引けば良い)
(0..n).each do |i|
  (0..n - i).each do |j|
    if 10000 * i + 5000 * j + 1000 * (n - i - j) == y
      puts "#{i} #{j} #{n - i - j}"
      exit
    end
  end
end
puts "-1 -1 -1"
```

- 白昼夢（https://atcoder.jp/contests/abs/tasks/arc065_a）
```
s = gets.chomp

# 先頭から順に読み上げていくと"dream"が"dreamer"に被ってしまう(prefixの関係)
# 後ろから順に分解する
s = s.gsub("eraser", "")
     .gsub("erase", "")
     .gsub("dreamer", "")
     .gsub("dream", "")
puts s.empty? ? "Yes" : "No" => puts s.length == 0 ? "YES":"NO" などでもOK
```
