## シェル環境  
## どうしてますか？

------------------------------------------------------------

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

------------------------------------------------------------

### みんなの入門 - bash -
- - -
一番多くのDistributionで使われている（？）  
いわゆる、de facto standardなshell。  
最近、頑張っているらしいです。  

|||||||||||||||

まさかの
<font style="color: yellow">**Windows10で対応**</font>  
(Windowsで使えるとは言っていない

|||||||||||||||

あとで、やるので詳細は省きます。  

------------------------------------------------------------

### 究極のシェル - zsh -
- - -
ズィーシェルっていいます。  
ダメ人間製造機  

|||||||||||||||

### オプションを調べたり覚えなくていい
- - -
「-」の後にtabキーで入力候補が出ます
<img src="./img/zsh/comp.jpg" style="width:75%"/>

|||||||||||||||

### gitの選択branchが表示される
- - -
わざわざgit branchとかいらない。  
<img src="./img/zsh/show_branch.jpg" style="width:50%"/>

|||||||||||||||

他にも
- bashとして振舞える(お前はいったい何なんだ  
- コマンド履歴を複数ターミナルに共有できる  

|||||||||||||||
<font style="font-size: 1.5em">
**何か裏があるんでしょ？**
</font>

|||||||||||||||

### 設定がメンドウ
- - -
<div style="float:left;">
	<img src="./img/zsh/zsh_code_l.jpg" style="width:50%"/>
</div>
<div style="float:right;">
	<img src="./img/zsh/zsh_code_r.jpg" style="width:50%"/>
</div>

|||||||||||||||

<font style="color:yellow; font-size: 1.5em">
**「仕事を楽にするためにzshを始めたのに**  
**時間を奪われてちっとも楽にならない」**  
</font>
と言われる。

|||||||||||||||

<font style="font-size: 2.0em">
**大体あってる。**
</font>

|||||||||||||||

つまり？

|||||||||||||||

<font style="color: yellow; font-size: 3.0em">**zshは宇宙**</font>  
意訳：頑張れば何でもできる

------------------------------------------------------------

### モダンシェル - fish -
- - -
Friendly Interactive SHell  
zsh  : 1990年（20世紀）  
fish : 2005年（21世紀）  
最近生まれた子。  
zshのカスタマイズ済版みたいな感じ

|||||||||||||||

### 強くてニューゲーム
- - -
WebUIによる簡単設定は、まさにバファ〇ン
<br>
<img src="./img/fish/web_config.png" style="width: 50%"></img>
<font style="margin: 0px; font-size: 0.75em">
※httpd / apache2とかがインストールされます
</font>
|||||||||||||||

### 秀逸な提案
- - -
fishはコマンドを覚えます。
<br>
<img src="./img/fish/autosuggestion.png"></img>
|||||||||||||||

### 補完がVisual Studio
- - - 
まるでIDEのIntellisense
<br>
<img src="./img/fish/git.png" style="width:50%"></img>
|||||||||||||||

<font style="font-size: 1.5em">
**欠点？**
</font>

|||||||||||||||

<img src="./img/bash/sonnamonohanai.jpg" style="width:50%"/>

|||||||||||||||

……すいません。  
ないわけではないです。  
（欠点というべきことか怪しいが

|||||||||||||||
### fishの欠点１- bash非互換 -
- - -
日本企業が愛する（？）<br>
<font style="color:yellow">**bashに互換性なし**</font>  
↓  
bash script使う度に  
fish上でbashを起動するのは大変ぽよー  
↓  
bash依存症の会社では無理ぽよ？  

|||||||||||||||
### fishの欠点２ - 情報量の少なさ -
- - -
Fishは最近の子ということもあって（？）  
zshお兄さんやbashおじさんと比べて  
全体的な情報量が少ない……気がします。  

|||||||||||||||

**Google人気ランキング！**  
**「○○sh 設定」で検索**  
※2016.1.15調べ  
<br>
<font style="margin: 0px; font-size: 0.75em">
※検索ワードが悪い気がしますが、気にしない
</font>
|||||||||||||||
<font style="margin: 0px; font-size: 1.5em">
**bash**  
**555,000件**
</font>
|||||||||||||||
<font style="margin: 0px; font-size: 1.5em">
**zsh**  
**180,000件**
</font>
|||||||||||||||
<font style="margin: 0px; font-size: 1.5em">
**fish**  
**988,000件**
</font>
|||||||||||||||

|順位|種類|件数|
|:--:|:--:|:---|
|1   |fish|988,000|
|2   |bash|555,000|
|3   |zsh|180,000|
<br>
予想を裏切り  
なぜかfishが栄冠の１位……  
(；ﾞﾟ'ωﾟ'):ｱ､ｱﾚ!?

|||||||||||||||

主観的な話ですが、  
スクリプト内での下記のやり方が若干違います。
- コマンドの実行
- 特殊変数
- 構文の書き方
<br><br>
でも、bashに比べて落とし穴がないので  
おとなしくドキュメント読んでください

------------------------------------------------------------

### ご注文はbashの強化ですか？
- - -

|||||||||||||||

### bashをモダンシェル並みに強化すると……
- bash知識<font style="color: cyan;">↑</font>
- 無駄作業<font style="color: cyan;">↓</font>
- bashの勉強時間<font style="color: red;">↑</font>
- Twitterする時間<font style="color: cyan;">↑</font>

|||||||||||||||

これから出てくるbash scriptは  
<font style="color: yellow; font-size: 1.5em">
Google Shell Style Guide  
</font>
にできるだけ準拠させています。

|||||||||||||||

### bash改善の構成
- - -
- aliasコマンドでオプションをデフォルトで
- bash関数で処理を自動化
- shoptで隠された力を開放する
- GNU readlineで闇の力も開放する
の４本立てです。

------------------------------------------------------------

### aliasを見直そう
- - -
`alias`は「コマンドを別名で登録する」コマンド。  
これを使ってみましょう。

|||||||||||||||

### human aliasesを重視する
- - -
<div style="text-align: left;">
“人に勧める”なら、それが何をするか分かるコマンド名にしよう。  
<br>
gitならこの人がオススメ  
Human Git Aliases  
http://gggritso.com/human-git-aliases
</div>

|||||||||||||||

### 対象外：短縮"するだけ"のコマンド
- - -
<div style="text-align: left;">
指の負担を緩和してくれ短縮コマンドは素晴らしい。  
しかし「短縮するだけ」のことに他人の意思や技巧は必要ない。  
各個人好きに短くしてください。  
</div>

|||||||||||||||

### 具体的にこんなのやりません
- - -
- 「emacs」->「e」  
macsの4文字を打つのが面倒だから短縮するという。  
勝手にしてくれ。  
- 「git status」->「gst」  
gstで何が起こるのか？  
作った本人にしか分からなそうぽよ……

------------------------------------------------------------

### オプションのデフォルト化
- - -

|||||||||||||||

唐突ですが

|||||||||||||||

コマンドオプションって  
覚えるの辛くないですか？

|||||||||||||||

### mv, cp, rmのオプション
- - -
<font style="font-size: 0.75em">

|オプション|効果内容|
|:--------:|:------------------------|
|-i        |上書きなどの際に確認が求められる|
|-I        |大量に消すときは確認しない      |
|-b        |上書き時に自動バックアップする  |
|--suffix="xxx"|バックアップ処理時のサフィックスを指定する|
|-v        |処理内容を出力する|

|||||||||||||||

まだ、わかる。  

|||||||||||||||

でも、メンドクサイ。  

|||||||||||||||

打ち間違えした日には  
**仕事する気**をロストしそう……

|||||||||||||||

### lessのオプション
- - -
<font style="font-size: 0.75em;">

|オプション|効果内容|
|:--------:|:------------------------|
|-g        |検索時、現在選択中の１つのみを色反転する|
|-i        |検索時、大小文字の区別をつけない|
|-M        |ファイル名、行数、進行率を表示する|
|-N        |左に行番号を表示する|
|-q        |エラーピープを無効化する|
|-R        |色付きで表示する|
|-s        |連続した空行を１行にまとめる|
|-S        |折り返さない。横スクロールを可能にする|
|-w        |空行を表す記号に~を表示しない|

|||||||||||||||

<div style="font-size: 2.0em;">

```bash
$ less -gMNRqw make.log
```

</div>
<div style="font-size: 1.0em">

…………？？

|||||||||||||||

明日には忘れている自信がある。

|||||||||||||||
やる気を失くす前に  
心が折れそうだ……  

|||||||||||||||

そうだ！  
システムに覚えさせよう！

|||||||||||||||

<font style="font-size: 1.0em">

```bash
alias rm='rm -Iv'
alias mv='mv -bv --suffix=".bak"'
alias cp='cp -bv --suffix=".bak"'
alias less='less -gMNRqW'
alias env='env | sort -f'

if [[ -x /usr/bin/dircolors ]]; then # 色情報ファイルに実行権限があれば
  alias ls='ls -FvX --color=auto --format=across --group-directories-first'
else
  alias ls='ls -FvX --format=across --group-directories-first'
fi
alias la='ls AB'
alias ll='clear && la -lh --color=auto --time-style="+%y-%m-%d %H:%M:%S"'

#bashrcのリロード処理。分かり易い名前で！
alias refresh='source $HOME/.bashrc && echo "Refresh Bash"'
```

|||||||||||||||

### オマケ：lsのオプション
- - -
<font style="font-size: 0.75em;">

|オプション|効果内容|
|:--------:|:------------------------|
|-A, --almost-all    |「.」「..」を除くすべてを出力する|
|-B, --ignore-backups|「~」などのバックアップファイルは出力しない|
|-F                  |ディレクトリ(/)、シンボリックリンク(@)、実行ファイル(*)、ソケット(=)などにそれぞれ記号をサフィックスする|
|-h, --human-readable|リスト表記などの単位表記を自動でMB/GB/TBに変換してくれる|
|-l        |リスト表記する|
|-v        |1,10,2,20...の並びを、1,2,10,20にしてくれる|
|-X, --sort=extension|拡張子別に並べる|
|--group-directories-first|最初にディレクトリを羅列する|
|--format=across/vertical|並び順を横方向もしくは縦方向に指定する|
|--time-style=""|日付表記を任意に指定する。（dateコマンドと同様に指定する）|

|||||||||||||||
------------------------------------------------------------

### cdしたら自動でlsする
- - -
<img src="./img/bash/cdls.png"></img>

|||||||||||||||

### 目的
- - -
1. cd解決時にディレクトリの内容を見せて欲しい。
2. cdを引数なしで解決しても、HOMEへ戻りたくない。<br>
   <font style="color: yellow">※偉大なMacintoshは移動しない。  </font>
3. lsをオシャレにしたい。

|||||||||||||||

### こんな感じにしてみた
- - -

``` bash
no_arg_no_act_cd_ls()
{
  local -r argc=$#
  if [[ ${argc} == 0 ]]; then
    return 1
  elif [[ 1 < ${argc} ]]; then
    echo "Too many args for cd command"
    return 1
  fi
  local -r argv=$@
  # \cd => builtin cd
  clear && \cd ${argv} && ls
}
alias cd='no_arg_no_act_cd_ls'
```

|||||||||||||||

### AND演算によるテクニック
- - -

<font style="font-size: 2.0em;">

``` bash
clear && \cd ${argv} && ls
```

</font>
<font style="font-size; 1.0em;">
&&(AND)は、全コマンドが真の場合のみ演算する。
<br>
1. cdが成功した場合、lsが実行される。  
2. cdに失敗した場合、lsは実行されない。  

|||||||||||||||

lsコマンドに関して  
`alias ls='xxx'`の後に、  
あの関数を定義すると  
aliasされたlsコマンドが適用される。



------------------------------------------------------------

もうエイリアスは  
それぞれで探してもらうとして

------------------------------------------------------------

### bashと秘密の機能
- - -
bashに隠された機能を開放したいと思います。  
zshに若干近くなります。  

------------------------------------------------------------

### 解放する方法 - shoptとは？ -
- - -

```bash
$ shopt           # オプション一覧が確認できる
$ shopt -s xxxxx  # xxxxxのオプションをONにする
$ shopt -u xxxxx  # xxxxxのオプションをOFFにする
```

|||||||||||||||

### cdコマンドすら使わない
- - - 
``` bash
shpot -s audocd
```

------------------------------------------------------------

### 意図を組むシェル
- - -
```bash
shopt -s cdspell
```

------------------------------------------------------------
|オプション名|内容|
|:---------:|:---------------|
|cdable_vars|見つからないディレクトリ名を変数名へ解釈する|
|dotglob    |*の展開に.が含まれるようになる          |
|extglob    |パターンマッチのワイルドカード表現が増える|
|globstar   |Rubyのように**で該当ディレクトリ以下のすべてのディレクトリ、ファイルに再帰的にマッチする|

------------------------------------------------------------

### Git Branch名をターミナルに出す
- - -
<img src="./img/bash/cdls.png"></img>

|||||||||||||||

### 目的
- - -
1. git branchとか打つのメンドウだよね
2. おしゃれでカッコイイじゃん
3. 間違えてcommitしたくない

|||||||||||||||

### 1.素材のダウンロード
- - -
<a href="https://github.com/git/git/blob/master/contrib/completion/git-prompt.sh">git-prompt.sh</a>  
<a href="https://github.com/git/git/blob/master/contrib/completion/git-completion.bash">git-completion.bash</a>  
※gitのインストールディレクトリから  
取得した方がいいかな

|||||||||||||||

### 2.実行権限を付与
- - -
```bash
$ chmod a+x git-prompt.sh
$ chmod a+x git-completion.sh
```

|||||||||||||||

### 3.プロンプトを変更する。
- - -

```bash
source $BASH_ROOT/git-completion.bash
source $BASH_ROOT/git-prompt.sh
# $(__git_ps1)がブランチ名を示す
PS1='${debian_chroot:+($debian_chroot)}\[\e[01:32m\]\u\[\e[00:37m\]@\h:\[\e[00:33m\]\w\[\e[00:37m\]|\[\e[03:31m\]$(__git_ps1)\[\e[00:37m\]\n\$ 
```

|||||||||||||||

<span lang="en" style="font-family: Arial;">
PS1='${debian_chroot:+($debian_chroot)}\\[\e[01:32m\\]\u\\[\e[00:37m\\\]@\h:\\[\e[00:33m\\]\w\\[\e[00:37m\\]|\\[\e[03:31m\\]$(__git_ps1)\\[\e[00:37m\\]\n\$ '
</span>  

|||||||||||||||

い、今のはいったい何の呪文なんだ……？？
<img src="./img/bash/prompt_wakaran.jpg" style="width: 40%"></img>

------------------------------------------------------------

### 逃げるは恥じゃないし役に立つ
- - -
制御シーケンス怖いので逃げます。  

|||||||||||||||

<font style="color:yellow">
制御シーケンスを生成する関数  
</font>
を作ってみた。

|||||||||||||||

### 仕様
- - -
文字列を受け取って解析して……  
ってのはメンドウなので、諸君らに頑張ってもらうとして。  

とりあえずは、  
01とか37mとかいうのをパラメータでもらって  
中で組み上げて文字列を返せばいいよね？

|||||||||||||||

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

|||||||||||||||

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

------------------------------------------------------------

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

------------------------------------------------------------

もっと知りたかったらどうぞ

------------------------------------------------------------

### おまけ

------------------------------------------------------------

### ラピ〇タの雷
- - -
<div style="text-align: left;">
通称、バルス  
Linux界隈に噂される魔の呪文（コマンド）  
</div>
<div style="font-size: 2.0em;">
``` bash
rm -rf /
```
</div>
ラピュ〇崩壊の呪文の名の通り、  
Linuxを崩壊させてくれる。

|||||||||||||||

やってみたい？  
これを読んでから、VMでやりなさい。  
http://lambdaops.com/rm-rf-remains/

|||||||||||||||

### 恐ろしい呪文から身を守る
- - -
ゴミ箱へ移動させるコマンドをインストールしよう  

```bash
$ sudo apt-get install trash-cli
```

|||||||||||||||

### あとはAliasしておく
- - -
```bash
if which trash ; then
	alias rm='trash-put'
else
	alias rm='rm -Iv'
fi

------------------------------------------------------------

### shoptをざっと紹介
- - -

### 


------------------------------------------------------------

### Reeadlineをざっと紹介
- - -
|キー     |readline関数名   |内容        |
|:-------:|:---------------:|:-----------|
|C-b / ← |backward-char    |１文字戻る  |
|C-f / → |forward-char     |１文字進む  |
|M-f      |forward-word     |１単語進む  |
|M-b      |backward-char    |１単語戻る  |
|C-u      |unix-line-discard|カーソル以前の文字列を削除|
|C-k      |kill-line        |カーソル以降の文字列を削除|
|C-r / ↑ |reverse-search-history|履歴を後方検索|
|C-s / ↓ |forward-search-history|履歴を前方検索|

|||||||||||||||

|キー     |readline関数名   |内容        |
|:-------:|:---------------:|:-----------|
|C-l      |clear-screen     |ターミナルクリア|  
|M-l      |downcase-word    |直後の単語を小文字へ|
|M-u      |upcase-word      |直後の単語を大文字に|
|C-i / tab|complete         |適した単語を補完|
|C-t      |transpose-chars  |前後の文字を入れ替える|


