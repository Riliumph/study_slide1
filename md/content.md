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
良くも悪くも普通。  
最近、頑張っているらしいです。  
あとで、やるので詳細は省きます。  
</div>

>>>

まさかのWindows10で対応  
(Winで使えるとは言っていない  


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

**何か裏があるんでしょ？**
>>>

### 設定がメンドウ
- - -
<div style="float:left;">
	<img src="./img/zsh/zsh_code_l.jpg" style="width:50%"/>
</div>
<div style="float:right;">
	<img src="./img/zsh/zsh_code_r.jpg" style="width:50%"/>
</div>
>>>

<font color="yellow">
「仕事を楽にするためにzshを始めたのに  
時間を奪われてちっとも楽にならない」  
</font>
と言われる。

>>>
**大体あってる。**
>>>

つまり？

>>>

##<font style="color: yellow">zshは宇宙</font>  
意訳：頑張れば何でもできる
---

### モダンシェル - fish -
- - -
<div style="text-align: left;">
Friendly Interactive SHellの略です。  
zsh  : 1990年（20世紀）  
fish : 2005年（21世紀）  
21世紀のシェルと言えるかもしれません。  
</div>
>>>

### 強くてニューゲーム
- - -
WebUIによる簡単設定は、まさにバファ〇ン。
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

### 欠点？
- - -

>>>

**そんなものはない。**

>>>

すいません。  
欠点と言うべきものか怪しいですが。  
ないわけではないです。

>>>

<font style="color:yellow">**bash非互換**</font>  
↓  
bash script使う度に  
fish上でbashを起動するのは大変ぽよー  
↓  
bash依存症の会社では無理かも？

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
短縮コマンドは素晴らしい。  
指の負担を緩和してくれます。  
しかし「短縮するだけ」のコマンドに他人の意思や技巧は必要ありません。  
各個人好きに短くしたらいいのです。  
</div>
>>>

### 具体的にこんなのやりません
- - -
- 「emacs」->「e」  
macsの4文字を打つのが面倒だから短縮するという。  
勝手にしてくれ。  
- 「git status」->「gst」  
gstで何が起こるのか？  
作った本人にしか分からなそうぽよ……

---

### aliasを見直そう
- - -
`alias`は「コマンドを別名で登録する」コマンド。  
これを使ってみましょう。
---

### fool proof
- - -
操作を誤っても危険が生じない  
または、  
そもそも危険な使い方ができない  
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
<aside class="notes">
これは、「/」と「.」が横にあるので気を付けなければならないコマンドです。
実行中のサーバーに対して呪文を唱えた大学の同期がいます。
ああ、大学のゼミサーバーでヨカッタヨカッタ
みんなの論文のリモートリポジトリが吹き飛んでしまいました。
</aside>

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
</div>
1. trashに成功したら、rm -ivは呼び出さない。
2. trashに失敗したら、rm -ivを呼び出す。
<br />
<font style="font-size: 22px;"
注意：<br />
エラーログを/dev/nullに捨ててるけど、問題の原因が分からなくなるのでお好きに。  
もっと言うと、whichコマンドで分岐した方がよろしいです。
</font>
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
<img src="./img/bash/cdls.png"></img>
<aside class="notes">
ディレクトリの中身は常に確認するモノ。  
ディレクトリの変更したら当然中身を見たいわけです。  
cdしたらlsするなんていうルーチンはシステムにでもやらせましょう。  
</aside>
>>>

### 目的
- - -
1. cd解決時にディレクトリの内容を見せて欲しい。
2. cdを引数なしで解決しても、HOMEへ戻りたくない。
   ※偉大なMacintoshは移動しない。  
3. lsをオシャレにしたい。
>>>

### こんな感じにしてみた
- - -

``` sh
no_arg_no_act_cd_ls()
{
	argc=$#
	if [ $argc -eq 0 ]; then
		return 1
	elif [ $argc -gt 1 ]; then
		echo "Too many args for cd command"
		return 1
	fi
	argv=$@
	# \cd => builtin cd
	\cd $argv && ls -Fv --group-directories-first
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
	argc=$#
	if [ $argc -eq 0 ]; then
		return 1
	elif [ $argc -gt 1 ]; then
		echo "Too many args for cd command"
		return 1
	fi
	argv=$@
	# \cd => builtin cd
	\cd $argv && ls -Fv --group-directories-first
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
色分けしてくれるけど、意味わからんのでね。
- <font style="color:yellow">-v</font>  
普通は 1,10, 2,20と整列されるところを  
正しく 1, 2,10,20と整列してくれる。  
- <font style="color:yellow">--group-directories-first</font>  
ディレクトリを順序の最初に持ってきてくれる。  
探すものによって見る場所を区切れるので便利。

---

もうエイリアスは  
それぞれで探してもらうとして
---


---
### Git Branch名をターミナルに出す
- - -
<img src="./img/bash/cdls.png"></img>

>>>

### 目的
- - -
1. git branchとか打つのメンドウだよね
2. おしゃれでカッコイイじゃん
3. 間違えてcommitしたくない

>>>

### 1.素材のダウンロード
- - -
<a href="https://github.com/git/git/blob/master/contrib/completion/git-prompt.sh">git-prompt.sh</a>  
<a href="https://github.com/git/git/blob/master/contrib/completion/git-completion.bash">git-completion.bash</a>  
※gitのインストールディレクトリから  
取得した方がいいかな

>>>

### 2.実行権限を付与
- - -
``` bash
chmod a+x git-prompt.sh
chmod a+x git-completion.sh
```

>>>

### 3.プロンプトを変更する。
- - -

```
source $BASH_ROOT/git-completion.bash
source $BASH_ROOT/git-prompt.sh
# $(__git_ps1)がブランチ名を示す
PS1='${debian_chroot:+($debian_chroot)}\[\e[01:32m\]\u\[\e[00:37m\]@\h:\[\e[00:33m\]\w\[\e[00:37m\]|\[\e[03:31m\]$(__git_ps1)\[\e[00:37m\]\n\$ 
```

>>>
<span lang="en" style="font-family: Arial;">
PS1='${debian_chroot:+($debian_chroot)}\\[\e[01:32m\\]\u\\[\e[00:37m\\\]@\h:\\[\e[00:33m\\]\w\\[\e[00:37m\\]|\\[\e[03:31m\\]$(__git_ps1)\\[\e[00:37m\\]\n\$ '
</span>  
>>>

<img src="./img/bash/prompt_wakaran.jpg" style="width: 50%"></img>

---

### 逃げるは恥じゃないし役に立つ
- - -
制御シーケンス怖いので逃げます。  

>>>

<font style="color:yellow">
制御シーケンスを生成する関数  
</font>
を作ってみた。

>>>

### 仕様
- - -
01とか37mとかいうのをパラメータでもらって  
中で組み上げて文字列を返せばいいよね？

>>>

### シーケンス生成関数
- - -
``` bash
### 制御シーケンスを作ってもらうよ！
GetStyle ()
{
    local font_type=$1
    local fg=$2
    local bg=$3
    case $# in
        1) echo "\[\e[${font_type}\]";;
        2) echo "\[\e[${font_type};${fg}\]";;
        3) echo "\[\e[${font_type};${fg}\e[${bg}\]";;
    esac
}
```
shellではreturnは0～255の1byte範囲の値のみ  
文字列を返したければ、echoなどの標準出力で返す。

>>>

``` bash
source $BASH_ROOT/git-completion.bash
source $BASH_ROOT/git-prompt.sh

GetStyle ()
{
    local font_type=$1
    local fg=$2
    local bg=$3
    case $# in
        1) echo "\[\e[${font_type}\]";;               # must W-quatation
        2) echo "\[\e[${font_type};${fg}\]";;         # must W-quatation
        3) echo "\[\e[${font_type};${fg}\e[${bg}\]";; # must W-quatation
    esac
}

GetPromptString ()
{
    local DEBIAN_INFO=${debian_chroot:+($debian_chroot)}
    local GIT_BRANCH='$(__git_ps1)'    # must single-quotation
    local white=$(GetStyle 00 37m)
    local B_lime=$(GetStyle 01 32m)
    local yellow=$(GetStyle 00 33m)
    local I_red=$(GetStyle 03 31m)
    echo "${DEBIAN_INFO}${B_lime}\u${white}@\h:${yellow}\w${white}|${I_red}${GIT_BRANCH}\n${white}\$ "
}

PS1=$(GetPromptString)
```

---

### 補足：クォートの違い？
- - -

``` bash
HELLO="Hello, Bash!."
echo "Double quote: ${HELLO}" # Double quote: Hello, Bash.
echo 'Single quote: ${HELLO}' # Single quote: ${HELLO}
```

- ダブルクォート  
  <font style="color:yellow">変数・関数を展開して</font>、文字列を認識する。
  
- シングルクォート  
  <font style="color:yellow">そのままの内容</font>を、文字列として認識する。
