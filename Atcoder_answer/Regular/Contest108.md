- A問題（https://atcoder.jp/contests/arc108/tasks/arc108_a）
```
# 自分の解答：TLE(Time Limit Exceeded)で指定された実行時間以内にプログラムが終了しなかった
s, p = gets.split(" ").map(&:to_i)
ans = "No"
 
(1..s).each do |n|
  (1..p).each do |m|
    if n + m == s && n * m == p
      ans = "Yes"
      break
    end
  end
end
puts ans
```
<br>

- 和の通りより積の通りから求めた方が良い
  - n*m のうち n<=mと仮定するとn<=√p となる(nが√pより大きいとmもpより大きくなりn*m>pとなってしまうから)
  - 小さい方(ここではn)を√pまで回せば良い
  - pがnで割り切れないとダメ(割り切れないとmがわからないから)
  
```
# 正解例
s, p = gets.split(" ").map(&:to_i)
ans = "No"

(1..p**(0.5)).each do |n|
    # n*m=pなのでp/n=m：n+(p/n)=n+m
    if p % n == 0 && n + (p / n) == s
      ans = "Yes"
      break
    end
end
puts ans
```
