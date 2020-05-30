---
title: Windows10で使える無料のRAM DISKソフト
author: スフィア
type: post
date: 2018-09-09T14:08:43+00:00
RelPermalink: /2018/09/windows10で使える無料のram-diskソフト/
image: /wp-content/uploads/2018/09/ramdisk_thumb.png
tw_card:
  - def
category_relation:
  - 'y'
tag_relation:
  - 'y'
disp_description_relation:
  - 'n'
page_layout:
  - def
menu_view:
  - 'y'
side:
  - 'y'
fullscreen_view:
  - 'n'
index:
  - index
follow:
  - follow
title_view:
  - 'y'
toc:
  - def
primary_category:
  - 142
ampforwp-amp-on-off:
  - default
ampforwp-redirection-on-off:
  - enable
pvc_views:
  - 1289
keni_layout_post:
  - layout-basic
keni_layout_post_sidebar:
  - layout-sidebar-basic
keni_layout_post_footer01:
  - layout-footer-show
keni_layout_post_footer02:
  - layout-footer-show
keni_layout_post_footer03:
  - layout-footer-show
keni_layout_post_navigation:
  - layout-navigation-show
keni_layout_post_breadcrumb:
  - layout-breadcrumb-show
keni_relation_post:
  - 'a:0:{}'
categories:
  - Windows10

---
[<img style="display: inline; background-image: none;" title="ramdisk" src="https://sumaho.tk/wp-content/uploads/2018/09/ramdisk_thumb.png" alt="ramdisk" width="244" height="164" border="0" />][1]

Asusにゲーム専用PC用のソフトだと思われます。スフィアはメインのデスクトップPCがAMDのCPUでマザーボードがAsusなのでこのソフトを数年前から使っていました。良いです。

今回、Lenovo Thinkpad SL-510でバッファローのRAM DISKを使おうと思ったらブルー画面になってしまい互換モードでもうまくいかなかったのでダメもとで試したら使えちゃったというお話です。

### 配布場所

Asusではもう配布していないのか？ゲーミングPCを購入された方のみに秘密のダウンロードが用意されているのかはわかりませんが、公式では見つからなかったです。

スフィアが昔DLしたファイルと同じものがネットにあったのでURLを公開しておきます。

セキュア通信でないサイトですのでリンクは載せません、必要なファイルは「RAMDisk\_Win7-81-10\_V20206.zip」です。

> http://ntwow.tistory.com/30

### このRAM DISKソフトの概要

実装RAMの中から適量の容量を選んでRAM DISKドライブを割り当てます。必要なアプリケーションフォルダなどをそのドライブにリンクすることで指定したアプリの高速化が期待できます。

[<img style="display: inline; background-image: none;" title="ramdisk2" src="https://sumaho.tk/wp-content/uploads/2018/09/ramdisk2_thumb.png" alt="ramdisk2" width="244" height="209" border="0" />][2]

容量を指定してドライブを作成

[<img style="display: inline; background-image: none;" title="ramdisk3" src="https://sumaho.tk/wp-content/uploads/2018/09/ramdisk3_thumb.png" alt="ramdisk3" width="244" height="208" border="0" />][3]

作成したドライブに高速化したいフォルダを割り当てることで高速化する。

何分古い仕様のThinkpad SL-510 なのでSATA2のバススピードが基本になりますが、その上でのRAM DISKドライブの速度テストが以下になります。

[<img style="display: inline; background-image: none;" title="ramdisk4" src="https://sumaho.tk/wp-content/uploads/2018/09/ramdisk4_thumb.png" alt="ramdisk4" width="244" height="223" border="0" />][4]

流石のスピードです。

今回は、Google chromeとOpenLiveWriterのみを指定していますが、このRAM DISKドライブにc:\windows\Tempなどを割り当てるのが最も効果を体感できるでしょう。

でも、そのまま登録してもダメです、現時点でc:\windows\Tempは作業用の一時フォルダとして機能しているので、設定を変更してあげる必要があります。以下に手順を簡単にイメージで紹介いたします。

<img class="alignnone wp-image-1291" src="https://sumaho.tk/wp-content/uploads/2018/09/ramdisk6.png" alt="" width="333" height="371" srcset="https://sumaho.tk/wp-content/uploads/2018/09/ramdisk6.png 479w, https://sumaho.tk/wp-content/uploads/2018/09/ramdisk6-270x300.png 270w" sizes="(max-width: 333px) 100vw, 333px" />

Windowsの環境変数を操作します。

<img class="alignnone wp-image-1292" src="https://sumaho.tk/wp-content/uploads/2018/09/ramdisk7.png" alt="" width="518" height="490" srcset="https://sumaho.tk/wp-content/uploads/2018/09/ramdisk7.png 618w, https://sumaho.tk/wp-content/uploads/2018/09/ramdisk7-300x284.png 300w" sizes="(max-width: 518px) 100vw, 518px" />

システム環境変数のTEMPとTMPの中身を一時的に変更します。

<img class="alignnone wp-image-1293" src="https://sumaho.tk/wp-content/uploads/2018/09/ramdisk8.png" alt="" width="518" height="490" srcset="https://sumaho.tk/wp-content/uploads/2018/09/ramdisk8.png 618w, https://sumaho.tk/wp-content/uploads/2018/09/ramdisk8-300x284.png 300w" sizes="(max-width: 518px) 100vw, 518px" />

**%SystemRoot%\TEMP**

これを、

**C:\Temp**

に変更します。その後、c:\にTempという空のフォルダを手動で作成します。

&nbsp;

これでシステム環境変数のTEMPとTMPの示す先は、C:\Tempになるのですが、一応、Windowsを再起動させたほうがよろしいと思いますので再起動させます。

再起動後。

<img class="alignnone wp-image-1294" src="https://sumaho.tk/wp-content/uploads/2018/09/ramdisk9.png" alt="" width="518" height="425" srcset="https://sumaho.tk/wp-content/uploads/2018/09/ramdisk9.png 639w, https://sumaho.tk/wp-content/uploads/2018/09/ramdisk9-300x246.png 300w" sizes="(max-width: 518px) 100vw, 518px" />

本来のシステム環境変数の場所をRAM Diskに登録し追加します。

<img class="alignnone wp-image-1295" src="https://sumaho.tk/wp-content/uploads/2018/09/ramdisk10.png" alt="" width="518" height="440" srcset="https://sumaho.tk/wp-content/uploads/2018/09/ramdisk10.png 660w, https://sumaho.tk/wp-content/uploads/2018/09/ramdisk10-300x255.png 300w" sizes="(max-width: 518px) 100vw, 518px" />

その後、必要なアプリも登録します。

<img class="alignnone wp-image-1296" src="https://sumaho.tk/wp-content/uploads/2018/09/ramdisk11.png" alt="" width="518" height="416" srcset="https://sumaho.tk/wp-content/uploads/2018/09/ramdisk11.png 641w, https://sumaho.tk/wp-content/uploads/2018/09/ramdisk11-300x241.png 300w" sizes="(max-width: 518px) 100vw, 518px" />

本来のシステム環境変数の場所のリンクをRAMDISK内に作成できたので、再度、システム環境変数TEMPとTMPの中身を、

**C:\Temp**

から

**%SystemRoot%\TEMP**

に戻してあげれば作業完了です。

お疲れ様でした。

&nbsp;

 [1]: https://sumaho.tk/wp-content/uploads/2018/09/ramdisk.png
 [2]: https://sumaho.tk/wp-content/uploads/2018/09/ramdisk2.png
 [3]: https://sumaho.tk/wp-content/uploads/2018/09/ramdisk3.png
 [4]: https://sumaho.tk/wp-content/uploads/2018/09/ramdisk4.png