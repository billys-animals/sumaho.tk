---
title: VAIO VGC-LB50についてのBIOS絡みの認識改め
author: スフィア
type: post
date: 2018-09-05T02:21:22+00:00
RelPermalink: /2018/09/vaio-vgc-lb50についてのbios絡みの認識改め/
image: /wp-content/uploads/2018/09/P_20180905_104832-246x200.jpg
categories:
  - パソコン
tags:
  - VGC-LB50

---
以前、ブログの記事でVGC-LB50は外部DVDドライブから起動できないと書きましたが間違いでした。外部USB機器からのブートができないと書きましたがこれも間違いでした。

<img class="alignnone wp-image-1265" src="https://sumaho.tk/wp-content/uploads/2018/09/P_20180905_104832.jpg" alt="" width="518" height="352" srcset="https://sumaho.tk/wp-content/uploads/2018/09/P_20180905_104832.jpg 806w, https://sumaho.tk/wp-content/uploads/2018/09/P_20180905_104832-300x204.jpg 300w, https://sumaho.tk/wp-content/uploads/2018/09/P_20180905_104832-768x522.jpg 768w" sizes="(max-width: 518px) 100vw, 518px" />

BIOSのページのアドバンスドで外部機器よりの起動を有効にします。

<img class="alignnone wp-image-1267" src="https://sumaho.tk/wp-content/uploads/2018/09/P_20180905_105136.jpg" alt="" width="518" height="319" srcset="https://sumaho.tk/wp-content/uploads/2018/09/P_20180905_105136.jpg 859w, https://sumaho.tk/wp-content/uploads/2018/09/P_20180905_105136-300x185.jpg 300w, https://sumaho.tk/wp-content/uploads/2018/09/P_20180905_105136-768x473.jpg 768w" sizes="(max-width: 518px) 100vw, 518px" />

その上でBOOT項目の優先順位からすべてを消去します（xを押すことで除外できます）

こうすることでかってに外部DVDや外部USB機器で起動できる媒体を探して起動します。

起動が終わり通常モードに直す場合は以下の様に設定し直します。

<img class="alignnone wp-image-1266" src="https://sumaho.tk/wp-content/uploads/2018/09/P_20180905_105100.jpg" alt="" width="518" height="253" srcset="https://sumaho.tk/wp-content/uploads/2018/09/P_20180905_105100.jpg 880w, https://sumaho.tk/wp-content/uploads/2018/09/P_20180905_105100-300x147.jpg 300w, https://sumaho.tk/wp-content/uploads/2018/09/P_20180905_105100-768x375.jpg 768w" sizes="(max-width: 518px) 100vw, 518px" />

USB Hard Diskが現れていますが、USBメモリーやUSB　HDDが刺さっていて且つ起動可能なメディアの場合は表示される様です。

**外付けのDVDや外付けのHDDから起動する場合は優先順位を空にするのがポイントです！**

&nbsp;