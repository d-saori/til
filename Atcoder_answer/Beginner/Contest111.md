- A問題（https://atcoder.jp/contests/abc111/tasks/abc111_a）

```
n = gets.chomp
puts n.gsub(/1|9/, "1" => "9", "9" => "1")

# 別解
# trメソッド：「（単一）文字」を置き換えるメソッド。文字列から指定の文字を変換したあとの文字列を返す。
# 文字列のインスタンス.tr("変換したい文字",  "置き換え文字")
n = gets.chomp
puts n.tr("19", "91")
```

- B問題（）
```
n = gets.to_i
puts ((n - 1) / 111 + 1) * 111

もしくは
n = gets.to_i
(n..999).each { |n|
  a = n.to_s.chars
  if a.uniq.size == 1
    puts n
    exit
  end
}
```
