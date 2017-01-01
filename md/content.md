## シェル環境  
## どうしてますか？
---

### シェルの種類
- - -
シェルっていっぱいありますよね。
- sh
<font color="yellow">
- bash
</font>
- csh
- ksh
<font color="yellow">
- fish
</font>
<font color="yellow">
- zsh  
</font>
↓こいつらは例外
- Windows shell
- Power shell
---

### みんなの入門 - bash -
- - -
<div style="text-align: left;">
一番多くのディストリで使われているであろうシェル。  
Win10で対応しました(Winで使えるとは言っていない  
良くも悪くも普通。  
最近、頑張っているらしいです。  
あとで、やるので詳細は省きます。  
</div>
---

### 究極のシェル - zsh -
- - -
<div style="text-align: left;">
ズィーシェルっていいます。  
bashとして振舞えます。(お前はいったい何なんだ  
とにかく入力補完がVisual Studioみたいに強力。  
ダメ人間製造機  
</div>
>>>

### オプションを調べたり覚えなくていい
「-」の後にtabキーで入力候補が出ます
![zsh補完](./img/zsh/comp.jpg)
>>>

### gitの選択branchが表示される
git branchが必要なくなります。
![zsh_show_branch](./img/zsh/show_branch.jpg)
>>>

### 何か裏があるんでしょ？
>>>

### 設定がメンドウ
<div style="float:left;">
	<img src="./img/zsh/zsh_code_l.jpg" style="width:60%"/>
</div>
<div style="float:right;">
	<img src="./img/zsh/zsh_code_r.jpg" style="width:60%"/>
</div>
>>>

### つまり？
- - -
##<font style="color: yellow">zshは宇宙</font>  
意訳：zshは頑張れば何でもできる
---

### 最近生まれたシェル - fish -
- - -
<div style="text-align: left;">
fishは2005年に誕生しました。  
zshが1990年ということを考えると、  
21世紀のシェルと言えるかもしれません。  
Friendly Interactive SHellの略です。  
</div>
>>>

### 強くてニューゲーム
- - -
fishの設定はバファ〇ンのように優しい。  
<font style="font-size: 75%">
※httpd / apache2とかがインストールされます
</font>
<img src="./img/fish/web_config.png" style="width: 80%"></img>
>>>

### 秀逸な提案
- - -
fishはあなたのコマンドを覚えます。
<img src="./img/fish/autosuggestion.png"></img>
>>>

### 強力な補完
- - - 
候補はカーソル選択でき、打つ必要すらありません。  
<img src="./img/fish/git.png" style="width:75%"></img>
>>>

### fish唯一の欠点？
- - -
<font style="color:yellow">**bash非互換**</font>  
↓  
bash script使う度に  
fish上でbashを起動するのは大変ぽよー  
↓  
bash依存症の会社では無理かも？
>>>

### もう  
### zsh/fishの劣化品を  
### bashで頑張るしかないのか…
---

### ご注文はbashの強化ですか？
- - -
>>>

### human aliasesを重視する
- - -
<div style="text-align: left;">
“人に勧める”なら、それが何をするか分かるコマンド名にしましょう。  
　  
gitならこの人がオススメ  
Human Git Aliases  
http://gggritso.com/human-git-aliases
</div>
>>>

### 対象外：短縮"するだけ"のコマンド
- - -
<div style="text-align: left;">
短縮コマンドは素晴らしい。指の負担を緩和してくれます。  
しかし「短縮するだけ」のコマンドに他人の意思や技巧は必要ありません。  
各個人好きに短くしたらいいのです。  
</div>
>>>

### 具体的にこんなのやりません
- - -
- 「emacs」->「e」  
macsの4文字を打つのが面倒だから短縮するという。  
- 「git status」->「gst」  
gstで何が起こるのか、それは作った本人にしか分からなそうぽよ……


---

### aliasを見直そう
- - -
`alias`は「コマンドを別名で登録する」コマンド。  
これを使ってみましょう。
---

### fool proof
- - -
<font style="color:yellow">
操作を誤っても危険が生じない  
</font>
または、  
<font style="color:yellow">
そもそも危険な使い方ができない  
</font>
そんな設計のこと。  
>>>
<font style="color:yellow">
**やってはいけないこと**  
**やってほしくないこと**  
</font>
は  
<font style="color:yellow">
**できなくしておきましょう。**  
</font>
ということ
>>>

人間がミスしないことを前提にした運用は必ず破綻する
頑張って○○しないようにするとかはバカバカしい
>>>

### ラピ〇タの雷
- - -
<div style="text-align: left;">
通称、バルス  
Linux界隈に噂される魔の呪文（コマンド）  
</div>

``` sh
rm -rf /
```

ラピュ〇崩壊の呪文の名の通り、  
Linuxを崩壊させてくれる。
>>>

やってみたい？  
これを読んでから、VMでやりなさい。  
http://lambdaops.com/rm-rf-remains/
>>>

### 恐ろしい呪文から身を守る
- - -
ゴミ箱へ移動させるコマンドをインストールしよう

``` sh
$ sudo apt-get install trash-cli
```

こうする

``` sh
alias rm='trash 2> /dev/null || rm -iv'  
alias mv='mv -bv --suffix=".bak"'  
alias cp='cp -bv --suffix=".bak"'  
```
>>>

### OR演算によるテクニック
- - -

``` sh
alias rm='trash 2> /dev/null || rm -iv'  
```

<div style="text-align: left;">
||(OR)は、一方が真の場合に演算する。  
つまり、  
1. trashに成功したら、rm -ivは呼び出さないし  
2. trashに失敗したら、rm -ivを呼び出す。  
<br />
<font style="font-size: 22px;"
注意：<br />
エラーログを/dev/nullに捨ててるけど、  
問題の原因が分からなくなるのでお好きに。
</font>
</div>
>>>

### オプションの詳細
- - -
- <font style="color:yellow">-i --interactive</font>  
すでに存在する場合、y/nの入力が必要になります。  
複数（4つ以上）指定した時に無視してほしいなら「-I」を使いましょう。
- <font style="color:yellow">-b --backup</font>  
上書き処理を行う場合、backupを残します。
- <font style="color:yellow">-S --suffix="xxx"</font>  
バックアップ時のサフィックスを指定します。
- <font style="color:yellow">-v --verbose</font>  
処理結果を表示する。  
---

### cdしたら自動でlsする
- - -
<div style="text-align: left;">
ディレクトリの中身は常に確認するモノ。  
ディレクトリの変更したら当然中身を見たいわけです。  
cdしたらlsするなんていうルーチンはシステムにでもやらせましょう。  
</div>
>>>

### builtinコマンドへの不満点
- - -
1. cd解決時にlsしてくれない。  
2. cdを引数なしで解決すると、HOMEへ戻る。  
   *偉大なMacintoshはそのままを維持する。
3. lsが見にくい。
>>>

### こんな感じにしてみた
- - -

``` sh
no_arg_no_act_cd_ls()
{
	if [ $# -eq 0 ]; then
		return 1
	elif [ $# -gt 1 ]; then
		echo "Too many args for cd command"
		return 1
	fi
	arg=$@
	# \cd => builtin cd
	\cd $arg && ls -Fv --group-directories-first
}
alias cd='no_arg_no_act_cd_ls'
```

<div style="text-align: left;">
<font style="color:yellow">
`\xx`でbuiltinコマンドがコールできる
</font>
</div>
>>>

### AND演算によるテクニック
- - -

``` sh
no_arg_no_act_cd_ls()
{
	if [ $# -eq 0 ]; then
		return 1
	elif [ $# -gt 1 ]; then
		echo "Too many args for cd command"
		return 1
	fi
	arg=$@
	# \cd => builtin cd
	\cd $arg && ls -Fv --group-directories-first
}
```

<div style="text-align: left;">
&&(AND)は、全コマンドが真の場合のみ演算する。
</div>
1. cdが成功した場合、lsが実行される。  
2. cdに失敗した場合、lsは実行されない。  
>>>

### オプションの詳細
- - -
- <font style="color:yellow">-F</font>  
種類ごとにサフィックスを表示してくれる。  
directory->[/]  
 sym-link->[@]  
exe->[*]  
etc...
- <font style="color:yellow">-v</font>  
普通は 1,10, 2,20と整列されるところを  
正しく 1, 2,10,20と整列してくれる。  
- <font style="color:yellow">--group-directories-first</font>  
ディレクトリを順序の最初に持ってきてくれる。  
探すものによって見る場所を区切れるので便利。
>>>

### こんな感じ
<img src="./img/bash/cdls.png"></img>
---

もうエイリアスは  
それぞれで探してもらうとして
---
