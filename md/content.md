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
Windows10でも使えます（使えるとは言っていない  
良くも悪くも普通  
最近、頑張っているらしいです  
あとで、やるので詳細は省きます。  
</div>
---
### 究極のシェル - zsh -
- - -
<div style="text-align: left;">
ズィーシェルっていいます。  
bashとして振舞えます。（お前は一体何なんだ  
とにかく入力補完がVSみたいに強力で、ダメ人間製造機です。  
</div>
--
### オプションを調べたり覚えなくていい
「-」の後にtabキーで入力候補が出ます
![zsh補完](./img/zsh/comp.jpg)
--
### gitの選択branchが表示される
git branchが必要なくなります。
![zsh_show_branch](./img/zsh/show_branch.jpg)
--
### 何か裏があるんでしょ？
--
### 設定がメンドウ
<div style="float:left;">![zsh_code](./img/zsh/zsh_code_l.jpg)</div>
<div style="float:right;">![zsh_code](./img/zsh/zsh_code_r.jpg)</div>
--
### つまり？
- - -
極めれば  
##<font style="color: yellow">zshは宇宙</font>  
---
## 最近生まれたシェル - fish -
- - -
fishは2005年に誕生しました。  
zshが1990年ということを考えると、  
21世紀のシェルと言えるかもしれません。  
Friendly Interactive SHellの略です。  
--
### 強くてニューゲーム
- - -
fishの設定はバファ〇ンのように優しい。
<img src="./img/fish/web_config.png"></img>
--
### 秀逸な提案
fishはあなたのコマンドを覚えます。
<img src="./img/fish/autosuggestion.png"></img>
--
### 強力な補完
候補はカーソル選択でき、打つ必要すらありません。  
<img src="./img/fish/git.png" style="width:75%"></img>
--
### fish唯一の欠点？
- - -
<font style="color:yellow">bash非互換</font>  
↓  
bash script使う度に  
fish上でbashを起動するのは大変ぽよ。  
↓  
bash依存症の会社では無理かも？
