---
title: Dopamineが最強の音楽プレーヤー～Error Code 2503
author: スフィア
type: post
date: 2018-08-17T00:31:18+00:00
image: /wp-content/uploads/2018/08/cmd3-246x200.png
aliases:
    - /2018/08/dopamineが最強の音楽プレーヤー～error-code-2503/
    - /post/2018/08/dopamineが最強の音楽プレーヤーerror-code-2503/

categories:
  - ソフトウエア

---
<a href="https://www.digimezzo.com/content/software/dopamine/" target="_blank" rel="noopener">Dopamine</a>という最強のミュージックプレーヤーを体験してWindows10でも試そうと思いインストールしようとすると「**Error Code 2503」で止まります。**

調べてみると「管理者権限でインストールする必要がある」のにそうしていないから出るエラーの様です。

<img class="alignnone wp-image-1171" src="https://sumaho.tk/wp-content/uploads/2018/08/cmd1.png" alt="" width="518" height="323" srcset="https://sumaho.tk/wp-content/uploads/2018/08/cmd1.png 647w, https://sumaho.tk/wp-content/uploads/2018/08/cmd1-300x187.png 300w" sizes="(max-width: 518px) 100vw, 518px" />

スタートメニュー -> Windowsシステムツール -> コマンドプロンプト -> その他 -> 管理者として実行

でコマンドプロンプトを管理者モードで起動します。

> **C:\WINDOWS\SYSTEM32>**

この状態でダウンロードフォルダのファイルを実行すると、

> **C:\WINDOWS\SYSTEM32>C:\Users\あなたのユーザー名\Downloads\Dopamine 1.5.14 (Release).msi**

実行できません。コマンドプロンプトなので、ドットや（）などの記号など入っていると実行できません。なので、名前をシンプルに変更します。

**Dopamine 1.5.14 (Release).msi　＝＞　Dopamine.msi**

この状態で以下の様に実行すると、

> **C:\WINDOWS\SYSTEM32>C:\Users\あなたのユーザー名\Downloads\Dopamine.msi**

&nbsp;

<img class="alignnone wp-image-1172" src="https://sumaho.tk/wp-content/uploads/2018/08/cmd2.png" alt="" width="333" height="260" srcset="https://sumaho.tk/wp-content/uploads/2018/08/cmd2.png 495w, https://sumaho.tk/wp-content/uploads/2018/08/cmd2-300x235.png 300w" sizes="(max-width: 333px) 100vw, 333px" />

インストール画面が立ち上がります。

<img class="alignnone wp-image-1173" src="https://sumaho.tk/wp-content/uploads/2018/08/cmd3.png" alt="" width="777" height="582" srcset="https://sumaho.tk/wp-content/uploads/2018/08/cmd3.png 950w, https://sumaho.tk/wp-content/uploads/2018/08/cmd3-300x225.png 300w, https://sumaho.tk/wp-content/uploads/2018/08/cmd3-768x575.png 768w" sizes="(max-width: 777px) 100vw, 777px" />

インターフェースはこんな感じでとにかく音が良いです。

FLACにも対応しているのが嬉しいです。

インターフェースの<a href="http://trackiss.hateblo.jp/entry/029/dopamine#pre2.0" target="_blank" rel="noopener">日本語対応はこちら</a>のサイトで配布されています。助かりますね。

&nbsp;

<iframe style="border: none;" src="https://rcm-fe.amazon-adsystem.com/e/cm?o=9&p=294&l=ur1&category=primemusic&f=ifr&linkID=1ae07ee4c8132fcdc5445aa1e8f2f183&t=pasokon-news-22&tracking_id=pasokon-news-22" width="320" height="100" frameborder="0" marginwidth="0" scrolling="no"></iframe>

松たかこさんの「five years singles」は大好きなアルバムなのですが、どうもCDからリッピングする時にソフトが悪かったのか？ちょと低音が強く高音がおとなしめに聞こえます。なので、ドンシャリ的なイコライザー（低音と高音をブーストする）できくと丁度良い感じになりました。

普段がイコライザーが嫌いで使わないのですが、このDopamineの様に本質的な音が良いソフトなのでイコライザーを使って良い意味で音を補正できるのですね。

[amazon\_link asins=&#8217;B00005R0Y1&#8242; template=&#8217;ProductLink&#8217; store=&#8217;pasokon-news-22&#8242; marketplace=&#8217;JP&#8217; link\_id=&#8217;94b51a49-a2e4-11e8-ac5b-39217efe18eb&#8217;]