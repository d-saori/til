- A問題(https://atcoder.jp/contests/abc168/tasks/abc168_a)

```
input = gets.to_i

num = input.length - 1
hon_num = [2, 4, 5, 7, 9]
pon_num = [0, 1, 6, 8]
bon_num = [3]

hon_num.map{ |hon| puts "hon" if hon.to_i == input[num].to_i}
pon_num.map{ |pon| puts "pon" if pon.to_i == input[num].to_i}
bon_num.map{ |bon| puts "bon" if bon.to_i == input[num].to_i}

もしくは

input = gets.chomp.to_s

if ['2', '4', '5', '7', '9'].include? input[-1]
  puts 'hon'
elsif ['0', '1', '6', '8'].include? input[-1]
  puts 'pon'
else
  puts 'bon'
end
```
