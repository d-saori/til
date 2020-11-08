- A問題（https://atcoder.jp/contests/abc182/tasks/abc182_a）

```
a, b = gets.split.map(&:to_i)

puts (2 * a + 100) - b
```

<br>

- B問題（https://atcoder.jp/contests/abc182/tasks/abc182_b）

```
def input_n
  gets.to_i               # 単一整数
end

def input_s
  gets.chomp              # 文字列。chompを付けないと改行文字がついてくる
end

def input_a
  gets.split.map(&:to_i)  # スペースで区切られた複数の整数
end

def input_o(num)
  num.times.map { gets.to_i }  # 縦に並んだ複数の整数。たまにある
end

def output_f(num)
  puts sprintf("%.12f", num)
end

n = input_n
a = input_a
gcds = Array.new(1001, 0)
max = a.max

(2..max).each do |i|
  a.each do |num|
    if num % i == 0
      gcds[i] += 1
    end
  end
end
puts gcds.index(gcds.max)

# 別例
n = gets.to_i
a = gets.split.map(&:to_i)
ans = (2..1000).max_by{ |r| a.count { |v| v % r == 0 }}
puts ans

```
