- Ruby学習のためにPCにローカル環境構築（VirtualBox、Vagrant）を行う

## ローカル開発環境を構築する必要が何故あるのか

- サーバーサイド言語（PHP、Ruby、Javaなど）は、サーバー側でプログラムを実行するので、サーバーへの接続を行う。<br>
そのためには、サーバーを借りる必要があるが、コストがかかってしまったり、手元のPCの情報を24時間インターネット上に公開するというデメリットもある。<br>
- それならば、同じ環境を自分のPC内に構築すれば、コストもかからず、ネット上に公開せずにWebアプリやWebサイトの開発、テストも行えて便利である。そのためには、手元に置いておける環境（ローカル環境）が必要になる。<br>
※ちなみにフロントエンド言語（HTML、CSS、JavaScript）は、ブラウザ上で動くため、サーバーとの通信を必要とせず、htmlファイルを用意しブラウザにドラッグ&ドロップすれば表示されるので、動作確認だけならブラウザとhtmlファイルがあれば可能であり、開発環境は必要ない。<br>
※またここでいきなり今回のテーマを壊しますが、ローカル環境構築を作るのではなく、ブラウザ上にサーバー環境を構築してくれるCloud9というサービスもある。



## ローカル環境構築までの流れ

**1. VirtualBoxをインストール**<br>
VirtualBox：仮想マシン本体ツール。手元のPCにいくつものサーバー（例えば1つを勉強用、もう1つを作りたいWebサーバーの開発用）を立ち上げることができる。<br>

**2. Vagrantをインストール**<br>
Vagrant:サーバーの設定やOSのインストール作業などをするのが複雑なVirtualBoxを、簡単なコマンドで扱えるようにしてくれるツール。
直接扱っていくのはVagrant、VirtualBoxは直接扱わないが、Vagrantコマンドを通じて裏でVirtualBoxは動いているというイメージ。

**３.サーバーを立ち上げる。**<br>
サーバー1つにディレクトリ（今回は『MyCentOS』）が1つ必要。（複数のサーバー＝複数のディレクトリをまとめられる大元のディレクトリ（今回は『MyVagrant』）を作成すると管理しやすい。）
MyCentOSディレクトリの中でサーバーを立ち上げ、サーバーの設定ファイルをVagrantのコマンドで作る（Vgrantfileを作りIPアドレスの設定などのサーバーの設定をする）
Vgrantfileの設定を読み込んで、裏でVirtualBoxを立ち上げてサーバーを作ってくれるという仕組み。<br>

**４.仮装マシンを立ち上げる**<br>
<br>
ターミナル起動

```
# ホームディレクトリに移動し、今後複数の仮想マシンを作ることを想定して、それらをまとめるディレクトリ（MyVagrant）を作る
~ $ cd
~ $ mkdir MyVagrant

# 作成したディレクトリ（MyVagrant）へ移動。（移動できてればプロンプト部分に『MyVagrant』と表示される）
~$ cd MyVagrant

# 仮想マシンを入れるディレクトリ（MyCentOS）を作り、移動。（移動できてればプロンプト部分に『MyCentOS』と表示される）
MyVagrant $ mkdir MyCentOS
MyVagrant $ cd MyCentOS

# 仮想マシンを設定するための『Vagrantfile』を作る
MyCentOS $ vagrant init bento/centos-6.8

# Vagrantfileを編集して仮想マシンのIPアドレスを192.168.33.10にする
MyCentOS $ sed -i '' -e 's/# config.vm.network "private_network", ip: "192.168.33.10"/config.vm.network "private_network", ip: "192.168.33.10"/' Vagrantfile

# 仮想マシンを起動
MyCentOS $ vagrant up

# 仮想マシンの状態を確認する。『running』と表示されれば仮想マシンが起動されている。
MyCentOS $ vagrant status
```


**５.仮想マシンの設定**<br>

```
# 立ち上げたサーバーにログインする（Vagrantfileのあるディレクトリから）
MyCentOS $ vagrant ssh

# サーバーが立ち上がりOSがインストールできたが、アプリケーションがインストールされていないので行う。OS最新状態にアップデートする。
[vagrant@localhost ~]$ sudo yum -y update

# スクリプト（プログラム）を入手するためのgitをインストール
[vagrant@localhost ~]$ sudo yum -y install git

# gitを使ってアプリケーション設定用のスクリプトをダウンロード。centos6ディレクトリが作成される。
[vagrant@localhost ~]$ git clone https://github.com/dotinstallres/centos6.git

# centos6フォルダへ移動
[vagrant@localhost ~]$ cd centos6

# スクリプトを実行
[vagrant@localhost centos6]$ ./run.sh

# 他の設定を反映
[vagrant@localhost centos6]$ exec $SHELL -l
```

**６.仮装マシン上のファイルを簡単に扱えるようにするため、ファイル転送ツール『Cyberduck』（FTPクライアントソフト）のインストールを行う**<br>

**７.仮想マシンにアクセスする**<br>
Cyberduckの『新規接続』→『SETP』→サーバーに上記で設定したIPアドレスを入力→ユーザ名、パスワード共に『vagrant』→接続
※今後も同じサーバーにアクセスしやすいようにブックマークしておくと便利。
→ブックマークメニュー→新規ブックマーク→ニックネームに『MyCentOS』で完了


**８.Ruby学習用のディレクトリ作成**<br>
右クリック→『新規フォルダ』→『Ruby_lessons』作成
『Ruby_lessons』へ移動→『新規ファイル（index.rb）』作成
この作成したファイルをクリックすると、設定したエディタが起動する。これでRubyを学習する環境の完成です。


## 補足
- 仮装マシンからのログアウト方法

・ブラウザやファイル転送ツールを終了させる<br>
・ターミナルにて<br>

```
# 仮想マシンからログアウトしMacの方へ操作が移る
[vagrant@localhost ruby_lessons]$ exit

# 仮装マシン停止
MyCentOS $ vagrant suspend

# ターミナル終了
MyCentOS $ exit
```

※ターミナルメニューにて『環境設定』→『プロファイル』→『シェル』→『シェルの終了時：シェルが正常に終了した場合は閉じる』に設定しておくと、ターミナル終了時に自動でウィンドウが閉じる<br>
※上記のように『exit』と入力しなくてもターミナルのウィンドウを閉じても終了はできるがコマンドを入力し正式に終了させる癖をつけておく<br>



- 仮想マシンに再びログインする方法

・ターミナル起動<br>

```
# ホームからMyVagrant（仮想マシンをまとめたディレクトリ）へ移動
~ $ cd MyVagrant

# MyVagrantからMyCentOS（仮装マシンのディレクトリ）へ移動
MyVagrant $ cd MyCentOS

# 仮装マシン起動
MyCentOS $ vagrant up

# 仮想マシンの状態確認（running表示でOK）
MyCentOS $ vagrant status

# 仮想マシンへログイン
MyCentOS $ vagrant ssh
（[vagrant@localhost ~]$となればログインできている）
```
