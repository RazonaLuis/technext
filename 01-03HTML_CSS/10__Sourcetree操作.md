# はじめに
Sourcetreeはプログラムのソースコードを管理するGitを簡単に扱うためのGUIツールです。
- add
- commit
- push
<br>
について実際に手を動かして操作をしながら、SourceTreeの使い方を習得していきましょう。

# 復習
## リポジトリとは
リポジトリファイルとはソース管理の基となるファイルで、「貯蔵庫」という意味になります。
ここにプロジェクト全体の変更点を保存しておき、ファイルをある時点の状態に戻したり、履歴を確認したりすることができるようになります。<br>
リポジトリファイルには２種類あります。
- ローカルリポジトリ
- リモートリポジトリ

### ローカルリポジトリ
作業中のPC内に存在するリポジトリファイルです。CommitというGitコマンドを使って、変更点の履歴を保存していきます。今回はローカルリポジトリを作成して、Sourcetreeで操作を行います。
.gitは隠しファイルなのでFinderで見ても存在するかわかりません。
ターミナルで隠しファイルを表示するオプションをつけてlsコマンドを実行することで確認できます。
### リモートリポジトリ
ソースを管理する為のサーバー上に存在するリポジトリファイルです。PushというGitコマンドを使って、ローカルリポジトリの履歴をサーバー上にUploadし保存することが可能です。
今回はリモートリポジトリの保存場所として「Github」というホスティングサービスを利用していきます。
### GitコマンドとSourceTree
ソース管理をおこうなう専用のコマンドです。使用するにはPCにGitソフトをインストールする必要がありますが、SourceTreeがインストールされているMacには改めてインストールする必要はありません。
Gitコマンドは通常、ターミナルからコマンドライン(CUI)ベースで実行するものなのですが、Gitコマンドを見やすい形で操作するためのツールがSourceTreeになります。

## 実践
早速実際にSourcetreeを使ってみましょう。

### COMMAND + SPACEでスポットライト検索
「SourceTree」と検索しましょう。<br>
![検索](./img/git/spotlight.png)

### ローカルリポジトリの作成とコードの記載
#### step1
起動し、「新規リポジトリ」ボタンを押し、「ローカルリポジトリの作成」をクリックします。<br>
![](./img/git/ope1.png)


#### step2
図の通り作業を進めてください<br>
リポジトリ作成場所はデスクトップフォルダの中に作成します。<br>
図のようにFinderのように『デスクトップ』という文字が少し薄黒くなっていれば問題ありません。
![](./img/git/ope2.png)


#### step3 
リポジトリ名の記載を求められるので『FirstGit』とし、作成をクリックしましょう。<br>
この作業が終われば**ローカルリポジトリの作成**完了です。
![](./img/git/ope3.png)

#### step4
ローカルリポジトリが本当に完成できているのか確かめましょう。
<br>
Finderを開いて、『デスクトップ』フォルダの中身をみてみましょう。<br>
![](./img/git/ope4.png)
<br>
FirstGitが確認できますね。

#### step5
SourcetreeでFirstGitを確認しよう。<br>
一度Sourcetreeを閉じてしまった方や、図のような一覧画面が表示されなくなってしまった方は、再度Sourcetreeを起動し直しましょう。<br>
スポットライト検索からSourcetreeを開けます。
図のように『FirstGit』が確認できれば、次の作業に進みましょう
![](./img/git/ope5.png)

#### step6
『FirstGit』をクリックすると下記の図のように表示がでます。<br>
しかし、**ファイルステータス**や**履歴**をクリックしても何も表示されていません。<br>
なぜでしょうか<br>
それもそのはず、実はまだリポジトリを作成しただけでファイルも用意していない、コードも記入していないためです。
![](./img/git/ope6.png)


#### step7
VS CODEからFirstGitを立ち上げましょう<br>
スポットライト検索からVS CODEを起動し、VS CODE上で**commmnad+o**を押し、開きたいフォルダを選択します。<br>
FirstGitを選択しましょう。
![](./img/git/ope7.png)

#### step8
コードを記入してみましょう<br>
ここでは簡単にhtmlの雛形を記載してみることにします。<br>
新規ファイル作成を行い、index.htmlを作成しましょう<br>
図のようになっていれば、次に進みましょう
![](./img/git/ope9.png)

#### step9
雛形だけの記載は味気ないので、bodyタグの中に図のように記載しましょう<br>
記載が終われば、ブラウザで開きましょう。
ブラウザで『はじめてSoureTreeを使用します』と表示がでることを確認してください
![](./img/git/ope12.png)

#### step10
Sourcetreeを確認してみましょう。（ファイルステータス）<br>
図のように、先程まで何も表示のなかったSourcetreeに雛形（自分がVS CODE上で記載したコード）が表示されました。
![](./img/git/ope14.png)

#### step11
- add
- commit
- push
をおこないましょう。

### add
![](./img/git/ope14.png)<br>
図の丸印にチェックをいれるとaddされます。<br>

### commit
commitメッセージを記載し、右下のコミットボタンをクリックしてcommitしましょう<br>
![](./img/git/ope50.png)<br>

左サイドバーの『ファイルステージ』から『履歴』に移動してみましょう。<br>
commitされたことが確認できます。<br>
![](./img/git/ope18.png)<br>

### push
次にpushボタンをおしてみましょう。<br>
図のような画面になることを確認してください<br>
![](./img/git/ope19.png)<br>
pushするブランチが何もないため,pushできません<br>
**リモートリポジトリが必要になります**<br>
それではリモートリポジトリを作成していきましょう。

### いままで結局なにをやってきたのか
ここまでの流れが,何かWebアプリを作成する時に行う作業です。<br>
ローカルリポジトリをSouretreeから作成し、実際にWebアプリを開発（今回は雛形に『はじめてSoureTreeを使用します』を記載した）。<br>
add、commitまで行いましが、リモートリポジトリが作成されていないのでpushできませんでした。リモートリポジトリを作成していきます。

### リモートリポジトリの作成

#### step1
自分のGithubアカウントにアクセスし、上部バーに記載にある＋ボタンをクリックしてみましょう。<br>
![](./img/git/ope20.png)<br>

#### step2
**New repository**を選択<br>
![](./img/git/ope21.png)<br>

#### step3
リポジトリ名を記載します。ここは自由に名前を記載できますが、今回はわかりやすく、ローカルリポジトリと同じ名前にしましょう。<br>
その他の項目については特に何も操作しなくて構いません。<br>
publicとprivateについてですが、publicに設定すると誰からでも閲覧が可能になります。<br>
privateは許可をしたユーザーのみが閲覧が可能になります。<br>
Create repositoryをクリックしましょう。<br>
ここまででリモートリポジトリの作成は終了です。
![](./img/git/ope22.png)<br>

### リモートリポジトリとローカルリポジトリの連携
#### step1
下記の図のように青く選択された部分をコピーします。
![](./img/git/ope24.png)<br>

#### step2
Sourcetreeでローカルリポジトリとリモートリポジトリを連携させます。<br>
設定→リモートの順に進んでいきます
![](./img/git/ope51.png)<br>
<br>
次に下図のように**リモートの名前:origin**、**URL / パス:先程GithubにてコピーしたURL**を貼り付けます。<br>
okを押して、さらに再度okがでますが、もう一度okをおします。
![](./img/git/ope26.png)<br>

#### step3
以上で連携は終了です。

### pushしましょう
先程はリモートリポジトリがなく、またローカルリポジトリとリモートリポジトリの連携もできていなかったため、pushできませんでした。<br>
ここまでカリキュラムを進められた方は、準備が整っています。pushしましょう。

### Sourcetree
pushボタンをおしましょう<br>
下記のようにチェックボックスとmasterという表示がでます。
masterにチェックをいれてOKをおしましょう。
![](./img/git/ope28.png)<br>

### push完了

### 最後にpushできていることを確認しましょう
GithubのFirstGitを選択して、以下の画像のように、index.htmlが表記されていれば成功です。
![](./img/git/ope30.png)<br>
<br>

## お疲れさまでした
何をやっているのかわからない、習得できるか不安という人もいるかもしれませんが、この作業は今後何回もやっていきますので、
慣れていきます。まずはパターン化して作業手順を覚えてしまいましょう。
<br>

## まとめ

- ローカルリポジトリの作成(Sourcetree)   
- リモートリポジトリの作成(Github)
- ローカルリポジトリとリモートリポジトリの連携(Githubで発行したURLをSourcetreeで登録)

