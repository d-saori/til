- A問題
```
c = gets.chomp
puts c == "a" || c == "e" || c == "i" || c == "u" || c == "e" || c == "o" ? "vowel" : "consonant"

# 別解
c = gets.chomp
puts "aeiou".include?(c) ? "vowel" : "consonant"
```
