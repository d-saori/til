superメソッド：親クラスのメソッドを呼び出す<br><br>

```
class Greeting
  def initialize()
    @msg = "good morning!"
    @name = "hoge"
  end

  def say_good_morning()
    puts "#{@msg} #{@name}"
  end
end

class Good < Greeting
  def say_good_morning()
  
    # puts "#{@msg} #{@name}"を呼び出している
    super()
    
    puts "YAHOO!"
  end
end

player = Good.new()
player.say_good_morning => good morning! hoge
                           YAHOO!
```
