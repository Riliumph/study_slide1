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
<img src="./img/fish/comletion.gif" style="width:60%"></img>

|||||||||||||||

### デバッガの標準装備
- - -


<div><!-- divタグがないと以降のimgタグが正常に動かない-->
<img src="./img/fish/debug.gif"
     onclick="this.setAttribute('src', this.getAttribute('src').replace(/_play.gif$/g, '.gif'));"
     style="cursor: pointer;">
</div>


|||||||||||||||


<font style="font-size: 1.5em">
**欠点？**
</font>

|||||||||||||||

<img src="./img/fish/sonnamonohanai.jpg" style="width:50%"/>

|||||||||||||||

……すいません。  
あります。  

|||||||||||||||

### fishの欠点- bash非互換 -
- - -
日本企業が愛する（？）<br>
<font style="color:yellow">**bashに互換性なし**</font>  
↓  
bash script使う度に  
fish上でbashを起動するのは大変ぽよー  
↓  
bash依存症の会社では無理ぽよ？  

|||||||||||||||

スーパーエンジニア達のつぶやき
<br>
<img src="./img/fish/002.png" style="width:40%"/>
<br>
<img src="./img/fish/001.png" style="width:40%"/>

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
に準拠させています。  
※できてなかったらツッコミお願いします。

|||||||||||||||

### この４本立てでやるよ！
- - -
- aliasコマンドでオプションをデフォルト化
- bash関数で処理を自動化
- shoptで隠された力を開放する
- ターミナルGNU readlineで闇の力も開放する

------------------------------------------------------------

### aliasを見直そう
- - -
`alias`は「コマンドを別名で登録する」コマンド。  
これを使ってみましょう。

|||||||||||||||

### human aliasesを重視する
- - -
“人に勧める”なら、それが何をするか分かるコマンド名にしよう。  
<br>
gitならこの人がオススメ  
Human Git Aliases  
http://gggritso.com/human-git-aliases

|||||||||||||||

### 対象外：短縮"するだけ"のコマンド
- - -
指の負担を緩和してくれる短縮コマンドは素晴らしいです。  
しかし「短縮するだけ」のことに他人の意思や技巧は必要ない。  
<font style="color: yellow; font-size: 1.5em">
各個人好きに短くしてください。  
</font>

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
|--suffix="xxx"<br>-S|バックアップ処理時のサフィックスを指定する<br>-Sの場合、環境変数SIMPLE_BACKUP_SUFFIXの設定値が使用される。<br>※未定義の場合、`~'|
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
|-q<br>-Q  |特定のエラーピープを無効化する<br>すべてのエラーピープを無効化する|
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

### aliasコマンド
- - -

<font style="font-size: 1.0em">

```bash
alias rm='rm -Iv'
alias mv='mv -bv --suffix=".bak"'
alias cp='cp -bv --suffix=".bak"'
alias less='less -gMNRqW'
alias env='env | sort -f'

if [[ -x /usr/bin/dircolors ]]; then # 色情報ファイルに実行権限があれば
  alias ls='ls -FvXx --color=auto --group-directories-first'
else
  alias ls='ls -FvXx --group-directories-first'
fi
alias la='ls -AB'
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

------------------------------------------------------------

### 関数で処理を自動化する
- - -

|||||||||||||||

### 目的
- - -
1. cd解決時にディレクトリの内容を見せて欲しい。
2. cdを引数なしで解決しても、HOMEへ戻りたくない。<br>
   <font style="color: yellow">※偉大なMacintoshは移動しない。  </font>

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

<div style="font-size: 2.0em;">

``` bash
clear && \cd ${argv} && ls
```

</div>
<div style="font-size: 1.0em;">
論理積(AND)演算は、正格評価(strict evaluation)される。
<br>
1. clear実行 ->（成功）-> cd実行 ->（成功）-> ls実行  
2. clear実行 ->（成功）-> cd実行 ->（失敗）
3. clear実行 ->（失敗）

|||||||||||||||

**lsコマンドに関して**
<br>
<br>
`alias ls='xxx'`の後に、あの関数を定義すると  
aliasされたlsコマンドが適用される。

|||||||||||||||

こんな感じの動き

|||||||||||||||

<div><!-- divタグがないと以降のimgタグが正常に動かない-->
<img src="./img/bash/cdls_play.gif"
     onclick="this.setAttribute('src', this.getAttribute('src').replace(/_play.gif$/g, '.gif'));"
     style="cursor: pointer;">
</div>

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

<div style="font-size: 1.5em;">

```bash
$ shopt           # オプション一覧が確認できる
$ shopt -s xxxxx  # xxxxxのオプションをONにする
$ shopt -u xxxxx  # xxxxxのオプションをOFFにする
```

|||||||||||||||

### cdコマンドすら使わない
- - - 
``` bash
shopt -s audocd
```
<div><!-- divタグがないと以降のimgタグが正常に動かない-->
<img src="./img/bash/autocd_play.gif"
     onclick="this.setAttribute('src', this.getAttribute('src').replace(/_play.gif$/g, '.gif'));"
     style="cursor: pointer;"></img>
</div>
※builtin cdが動くのが難点。

|||||||||||||||

### 意図を組む移動
- - -
```bash
shopt -s cdspell
```

<div><!-- divタグがないと以降のimgタグが正常に動かない-->
<img src="./img/bash/cdspell_play.gif"
     onclick="this.setAttribute('src', this.getAttribute('src').replace(/_play.gif$/g, '.gif'));"
     style="cursor: pointer;"></img>
</div>
 ※builtin cdが動くのが難点。

|||||||||||||||

### ざっくり紹介
- - -

<font style="font-size: 0.75em;">

|オプション名|内容|
|:---------:|:---------------|
|cdable_vars|見つからないディレクトリ名を変数名へ解釈する|
|dotglob    |*の展開に.が含まれるようになる          |
|extglob    |パターンマッチのワイルドカード表現が増える|
|globstar   |**で起点以下のすべてのディレクトリ、ファイルに再帰的にマッチする<br>Rubyライク？|
|etc...|

------------------------------------------------------------

### GNU readline
- - -
CUIプログラムにおいてコマンド履歴機能やTABキーによる補完機能を実現するのに使われるGPLライブラリ。  
bashの補完時の処理を変更することができる。

<font style="font-size: 1.5em;">

```bash
~/.inputrc # デフォルトでは、ここのファイルを見に行く
INPUTRC=xxxx # 環境変数INPUTRCがあれば、それを見に行く
```

|||||||||||||||

こういうのがreadlineの機能

<font style="font-size: 0.75em;">

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
|C-l      |clear-screen     |ターミナルクリア|
|C-i / tab|complete         |適した単語を補完|
|etc..|

|||||||||||||||


### bashの補完はコレがダメ
- - -

- 補完表示にtabを<font style="color: yellow">2回</font>も押す必要がある
- tab連打で<font style="color: yellow">入力補完してくれない</font>  
- <font style="color: yellow">色が付いてない</font>から良くわからない  
- <font style="color: yellow">サフィックスがディレクトリだけ</font>っぽい<br>
※ディレクトリへのシンボリックリンクも「/」が付く 

|||||||||||||||

### 設定例
- - -

``` bash:inputrc
# readline対応ソフト全部に適応されるので「bashのみ」を条件に分岐しておく
$if bash
  # TABキーに「一覧表示から補完する関数」を割り当てる
  TAB: menu-complete
  # TAB１回目：補完一覧 / ２回目；補完開始
  set show-all-if-ambiguous on
  # 補完一覧を色付け
  set colored-stats on
  # 補完一覧にサフィックス付与
  set visible-stats on
  # シンボリックリンクには「@」を付与
  set mark-symlinked-directories on
$endif
```


|||||||||||||||

<div><!-- divタグがないと以降のimgタグが正常に動かない-->
<img src="./img/readline/comletion_play.gif"
     onclick="this.setAttribute('src', this.getAttribute('src').replace(/_play.gif$/g, '.gif'));"
     style="cursor: pointer; width:70%;"></img>
</div>
※readlineのリロードは「C-x, C-r」

|||||||||||||||

えっ？！  
fishみたいにカーソル移動で  
選択できないんですか！？

|||||||||||||||

……そんなこと言っちゃういじわるな人は  
今すぐpecoを導入すればいいと思いますまる  
<br>
<br>
※pecoはオマケで扱います。

|||||||||||||||

やってもいいかなって思うモノを列挙してみました。  
じぶんでかくにんしてね？  
<br>
ここが詳しい  
http://www.geocities.jp/harddiskdive/gdb/gdb_354.html

|||||||||||||||

<font style="font-size: 0.75em;">

|readline関数名         |内容            |
|:---------------------:|:---------------|
|completion-ignore-case |onならファイル名補完で大文字と小文字を無視する。|
|completion-map-case    |onなら補完時に"-"と"_"を区別しない。|
|expand-tilde|ワード補完の際にチルダを$HOMEの内容に展開する。
|match-hidden-files<br>(default on)|.から始まるファイルも補完候補に加える。|
|page-completions<br>(default on)  |候補が画面をはみ出すときにmoreライクなページ送りを利用する。|
|print-completions-horizontally    |画面の下方向ではなく、水平方向にアルファベット順に並べて補完候補を表示する。|
|show-all-if-unmodified|部分的な補完が出来ない場合でも補完する。<br>これはonにするべき。|
|skip-completed-text   |被った部分を削除する。※＿はカーソル位置<br>ex) Make＿file -> (tab) -> ×Makefilefile　〇Makefile |


|||||||||||||||

<font style="font-size: 0.75em;">

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
|C-l      |clear-screen     |ターミナルクリア|
|M-l      |downcase-word    |直後の単語を小文字へ|
|M-u      |upcase-word      |直後の単語を大文字に|
|C-i / tab|complete         |適した単語を補完|
|C-t      |transpose-chars  |前後の文字を入れ替える|

|||||||||||||||

他にも便利なのいっぱいあるけど、もうあきらめた。  
調べてください。

|||||||||||||||






|||||||||||||||






------------------------------------------------------------

### Git Branch名をターミナルに出す
- - -
<img src="./img/bash/cdls_play.gif"></img>

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

|||||||||||||||

な、何がなんだかよくわからねぇが  
あんな感じで書けばいいんだな？
<br>
<br>
あんなもの人が書くモノじゃねぇよ
と思った人は、オマケをご参照ください。

------------------------------------------------------------

<div><!-- divタグがないと以降のimgタグが正常に動かない-->
<img src="./img/etc/thank_you_for_listening_cool_play.gif"
     onclick="this.setAttribute('src', this.getAttribute('src').replace(/_play.gif$/g, '.gif'));"
     style="cursor: pointer;"></img>
</div>

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
if which trash &> /dev/null ; then
	alias rm='trash-put'
else
	alias rm='rm -Iv'
fi
```
------------------------------------------------------------

### shoptをざっと紹介
- - -

### 


------------------------------------------------------------
