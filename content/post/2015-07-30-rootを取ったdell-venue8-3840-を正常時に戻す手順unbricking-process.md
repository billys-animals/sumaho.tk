---
title: ROOTを取ったDELL Venue8 3840 を正常時に戻す手順(Unbricking Process)
author: スフィア
type: post
date: 2015-07-30T06:35:00+00:00
RelPermalink: /2015/07/rootを取ったdell-venue8-3840-を正常時に戻す手順unbricking
categories:
  - アンドロイド
tags:
  - スマートフォン
  - DELL
  - タブレット
---
これが正解だったかどうかは良く分かりませんが、とりあえず、一旦はルートを取り、デルのファームウエアの更新も出来なくなったVenue8 3840を最新の状態に戻せたので備忘録的に書いておきます。

## Index of /releases/Venue\_8\_3840_Merrifield/developer-edition


(http://opensource.dell.com/releases/Venue_8_3840_Merrifield/developer-edition/)

おそらく、一番最初の初期状態に戻すには、↑の直下の

1. IFWI_MERR_PRQ_UOS_TH2_YT2_ww27_001.bin
1. droidboot.img.POS.bin 18-Mar-2015 16:58 15M
1. fwr_dnx_PRQ_ww27_001.bin 18-Mar-2015 16:58 96K
1. osr_dnx_PRQ_ww27_001.bin

この４つファイルを使うと思います。


今回、当方はこれでなく最新版を使いました。

(http://opensource.dell.com/releases/Venue_8_3840_Merrifield/developer-edition/A195/Unbrick/)


YTP802A119500-2014-07-16-22.tgz
これをＤＬして解凍して出来た、

1. ifwi_PRQ.bin
1. droidboot.img.POS.bin
1. dnx_fwr_PRQ.bin
1. dnx_osr_PRQ.bin
を使いました。


具体的には、
(http://opensource.dell.com/releases/Venue_8_3840_Merrifield/developer-edition/FlashTool/)
この直下の、
1. IntelAndroidDrvSetup1.5.0.exe
1. P708T_Driver_V1.0.0.msi
1. iSocUSB-Driver-Setup-1.0.4.zip
1. xFSTK_downloader_1.5.1.zip
を解凍なりして、インストールした後で、

xFSTK-Downloaderを実行します。

その後、準備Ｐａｒｔ２という事で、

(http://opensource.dell.com/releases/Venue_8_3840_Merrifield/developer-edition/FlashTool/fastboot/)

ローカルに「fastboot」フォルダを作成してその中に
以下のファイルを全てＤＬして全部保存して下さい。
加えて、YTP802A119500-2014-07-16-22.tgz解凍したファイルも全てこのfastbootフォルダにも
コピーしておいて下さい。
![](http://sumaho.tk/wp-content/uploads/2015/07/dell_restore01.jpg)

設定画面で赤枠の中のパスを↑でＤＬして解凍したファイルを指定します。


①タブレットの電源は落としておきます。
②その次に、タブレットのボリューム↑ボタンを押しながらＵＳＢケーブルでパソコンとタブレットを繋ぎます。
➂青枠の「Begin Download」ボタンを押します。
  ↓のProgressが変化してDeviceStatusも変わっていきます。
  ここまで終わるとかってに再起動して、ＤＥＬＬロゴでなくIntelロゴで起動してＦａｓｔＢｏｏｔモードで立ち上がります。
➃fastbootフォルダ内の「P802_flash_device_wifi_only.bat」を実行するとこのフォルダ内の対象ファイルがタブレットに適用されていきます。最終的に全部処理が終わるとタブレットは自動的に再起動されて一番最初の様に初期設定画面から設定することになります。


> **最初：
  
> AndroidVersion :4.4.2
  
> 0005.1172
  
> YTP802A195500**
> 
> 最初の更新：
  
> AndroidVersion :4.4.4
  
> 0005.2233
  
> YTP802A142000
  
> 2度目の更新：
  
> AndroidVersion :4.4.4
  
> 0005.2235
  
> YTP802A153000


といった様にＤＥＬＬのファームウエアの更新が適用出来る様になりました。
でも、やっぱりGoogleChromeは何か重いし、コレだったら前のままで良かったかもしれないとも思っております。
 次のファームウエア更新（あるかな？）に期待かもです。
