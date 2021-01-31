- 五目並べ
```
$board = 5.times.map { gets.chomp.chars }

# 連続で5つ並んでいるか確認する処理
def aligned?(o, x)
  if o == 5
    'O'
  elsif x == 5
    'X'
  else
    'D'
  end
end

# 行の確認
def row_aligned?
  result = ''

  $board.each { |row|
    o = 0
    x = 0
    (0..4).each { |i|
      if row[i] == 'O'
        o += 1
      elsif row[i] == 'X'
        x += 1
      else
        break
      end
    }

    result = aligned?(o, x)
    break if result != 'D'
  }

  result
end

# 列の確認
def col_aligned?
  result = ''

  (0..4).each { |i|
    o = 0
    x = 0
    $board.each { |col|
      if col[i] == 'O'
        o += 1
      elsif col[i] == 'X'
        x += 1
      end
    }

    result = aligned?(o, x)
    break if result != 'D'
  }

  result
end

# 斜めの確認
def oblique_aligned?
  result = ''

  (0..1).each { |obl|
    i = 0

    if obl.zero?
      j = 0
    else
      j = 4
    end

    o = 0
    x = 0
    (1..5).each {
      if $board[i][j] == 'O'
        o += 1
      elsif $board[i][j] == 'X'
        x += 1
      end

      i += 1

      if obl.zero?
        j += 1
      else
        j -= 1
      end
    }

    result = aligned?(o, x)
    break if result != 'D'
  }

  result
end

if row_aligned? == 'O' || col_aligned? == 'O' || oblique_aligned? == 'O'
  puts 'O'
elsif row_aligned? == 'X' || col_aligned? == 'X' || oblique_aligned? == 'X'
  puts 'X'
else
  puts 'D'
end
```
