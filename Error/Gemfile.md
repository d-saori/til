CRUDアプリを作成時<br>

```
$ bundle exec rake db:create
```
実行後、下記のメッセージ<br>

```
Your Ruby version is 2.6.5, but your Gemfile specified 2.7.0
```

GemfileのRubyバージョンを2.6.5へ変更すれば良いのだと思い、以下を実行<br>

```
$ vi Gemfile
#Rubyのバージョンを2.7.0から2.6.5へと編集
```

編集後、再び`bundle exec rake db:create`を実行したところ、今度は以下のメッセージ。<br>

```
Could not find rake-13.0.1 in any of the sources
Run `bundle install` to install missing gems.
```

指示通りに以下を実行<br>

```
$ bundle install
```

3度目の正直で再び`bundle exec rake db:create`を実行したところ…<br>

```
Created database 'crud_sample_development'
Created database 'crud_sample_test'
```


railsコマンドの場合だけは、railsもbundle exec railsも、同じ動作となる。Railsそのものが、プロジェクトルートを読み込んで、適切な実行を行ってくれるから。<br>
ただし、Rubyにrails gemを入れていない（Bundler管理の分しかない）環境では、railsコマンドが存在しないので、実行がそもそもできない（bundle exec rails もしくはbin/railsとなる）。<br>

一般には、xxxコマンドとbundle exec xxxで実行されるものは異なる。<br>

bundle install とは、bundlerというgemを使って、Gemfileの記載内容に従ってgemをインストールするためのコマンド。<br>
まずbundlerというgemをインストールするとbundleというコマンドが有効になる。bundlerはbundle installの他にもbundle update等、様々なgem管理コマンドを提供する。<br><br>

bundlerを用いることで、「システム開発のために必要なgemの管理」を簡単にすることができる。<br><br>

例えば複数人で開発する時、Gemfileを作ってそれを全員で共有すれば、後はbundle install一発で必要なgemが全てインストールできる。後から必要なgemが増えた場合も、Gemfileを更新してから各々bundle installを再実行すれば、常に全員同じ環境を確保できる。<br>
一人で開発している場合でも、例えば普段は自宅のデスクトップPCで作業していたけれど、新しくノートPCに開発環境を作りたいという時にbundle install一回で必要なgemが揃う。<br><br>

その他、利用するgemのバージョン管理(最新版だと動かないので、少し古いバージョンを使いたい等)や、開発orテスト環境でだけインストールするgemを設定する等、個別のgem installでは煩雑になってしまう作業も、bundlerならGemfile一つで全て管理できる。<br><br>

bundle installは、現在居るディレクトリ内にある、Gemfile.lockの内容に従ってライブラリをインストールするコマンド。
