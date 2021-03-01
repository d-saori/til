- A問題
```
c = gets.chomp
puts c == "a" || c == "e" || c == "i" || c == "u" || c == "e" || c == "o" ? "vowel" : "consonant"

# 別解
c = gets.chomp
puts "aeiou".include?(c) ? "vowel" : "consonant"
```

- B問題
```
h, w = gets.split.map(&:to_i)
(0..h).each { |i|
  c = gets.chomp
  puts c
  puts c
}

# 別解
h, w = gets.split.map(&:to_i)
puts h.times.map { gets * 2 }.join
```
