- A問題（https://atcoder.jp/contests/abc117/tasks/abc117_a）

```
t, x = gets.split.map(&:to_f)
puts t / x
```

- B問題
```
n = gets.to_i
l = gets.split.map(&:to_i).sort.reverse
puts l[0] < l[1..-1].sum ? "Yes" : "No"
```

- C問題
```
n, m = gets.split.map(&:to_i)
x = gets.split.map(&:to_i).sort
# コマの数が目的地以上の場合(n>m)、各目的地に1つ以上のコマを配置できるので移動は0回
# n<mで、コマが1つの場合は、区間の一端(最小値)に配置し、もう一端(最大値)に移動するのが最適
# n<mで、コマが複数の場合は、複数のコマが同じ座標を訪れるのは無駄。
# 各コマが担当する区間を並べると、ちょうどn-1個の開区間(xi, xi+1)が訪れていない形になるので、l=xi+1 - xiとすると、その時の合計移動回数は(xm-x1)-(訪れられていない開区間のliの和)となる為、(訪れられていない開区間liの和)を最大化すれば良い
# liを大きい方からn-1個取るのが最大
ds = []
0.upto(x.size-2) { |i|
  ds << x[i+1] - x[i]
}
ds.sort!
puts (ds[0..-n].sum || 0)
```
