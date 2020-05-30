---
title: BIOSでIDEをAHCIに変更するとWindows10が起動できない
author: スフィア
type: post
date: 2018-07-23T06:24:30+00:00
RelPermalink: /2018/07/biosでideをahciに変更するとwindows10が起動できない/
image: /wp-content/uploads/2018/07/mother_bord01-246x200.jpg
categories:
  - Windows
tags:
  - ide
  - ahci
  - bios
  - efi
  - ブルー画面
  - エラー
---

新たに換装したSSDの性能を引き出す為に、今まで放っておいたSATAの設定を直そうと思いました。

Windows10の自作機でBIOSを起動させ、Sataの接続を、IDEからAHCIに変更するとWindws10が起動できない、あの嫌なブルー画面（QRコード付きの）が表示されてしまいます。

<img class="alignnone size-full wp-image-537" src="https://sumaho.tk/wp-content/uploads/2018/07/qrcode.png" alt="" width="255" height="82" />

自動再起動しても、修復オプションを設定しても、セーフモードでも、何をやっても消えません。仕方なくBIOSの設定を元のIDEに変更すると正常に起動します。

## 考えた原因と対策

Sata1とSata2が混在していたり、別途拡張SlotでIDEのHDDを接続していたので、先ずは、IDE接続用の拡張Slottを外し旧式のATA接続のHDDを外しました。

**　　＝＞何も変化なし。**

次に考えたのが、Sata1 1.5gタイプのHDDを6gタイプのSSDの混在が原因かもしれないと思い、1.5gタイプを外そうか？と考えたが実際に運用上困るので躊躇していました。

別のノートＰＣでもやはり、IDEモードで動いていたので、BIOSの設定で、これをAHCIに変更すると、やはりブルー画面でエラーとなりました。

この時点で、複数Sataバージョン混在が原因をいう説は完全否定されます。なぜなら、そのノートパソコンがCrucial SSD M4しか接続されていないからです。

と、いう事は、BIOS側で他にも設定が必要な箇所があるかどうか？とWindowsの設定が問題かも知れないと思いました。

検索すると直ぐに答えが見つかりました。

<a href="http://capacitor.jp/blog-entry-253.html" target="_blank" rel="noopener">　　　Windows 10でAHCIへ変更（SSD等に入替えた時)</a>

こちらの記事の通り、レジストリの設定を変更する事で正常にAHCIモードで起動出来る様になりました。
逆に、AHCIモードで動いている状態から、EFI（BIOS)の設定をIDEモードに変更すると最初のブルー画面が表示されて起動出来ません。
Windowsの設定が↑のレジストリ調整でAHCIモードになっているのでエラーになるのでしょう。
つまり、EFI（BIOS)とWindowsのレジストリの両方を、IDEとかAHCIに寄せて揃えてあげないと正常起動しないって事ですね。

ちなみに先日、デスクトップ自作パソコンのマザーボードのEFI（BIOS)を更新しました。そのせいでEFI（BIOS)は初期化されAHCIモードに変更しておいた設定も初期化されIDEに戻ってしまいました。案の定、上のブルー画面になり、EFI（BIOS)の設定でIDEをAHCIに変更する事で解決しました。
 
## IDEモードとAHCIモードでのSSD速度結果

せっかくなので、IDEモードで測定したSSDの結果と、AHCIモードでの結果を載せておきます。

<img class="alignnone wp-image-89 size-medium" src="https://sumaho.tk/wp-content/uploads/2018/06/crucial_mx300_info-300x274.jpg" alt="" width="300" height="274" srcset="https://sumaho.tk/wp-content/uploads/2018/06/crucial_mx300_info-300x274.jpg 300w, https://sumaho.tk/wp-content/uploads/2018/06/crucial_mx300_info.jpg 402w" sizes="(max-width: 300px) 100vw, 300px" /><img class="alignnone wp-image-538 size-medium" src="https://sumaho.tk/wp-content/uploads/2018/07/crucial_mx300_ahci001-300x274.png" alt="" width="300" height="274" srcset="https://sumaho.tk/wp-content/uploads/2018/07/crucial_mx300_ahci001-300x274.png 300w, https://sumaho.tk/wp-content/uploads/2018/07/crucial_mx300_ahci001.png 402w" sizes="(max-width: 300px) 100vw, 300px" />

左がIDEで右がAHCIモードです。SSDはCrucialMX300 275GBです。

期待していたほどの効果は無いようですね。ただ、地味に性能は上がったので嬉しいことです。このままの設定で運用します。

その状態で<a href="https://sumaho.tk/2018/06/crucial-mx300%e3%80%80275gb-ssd-%E8%B3%BC%E5%85%A5%E3%83%AC%E3%83%93%E3%83%A5%E3%83%BC/" target="_blank" rel="noopener">Crucial Storage Executive</a>を使って一時キャッシュ適用後のクリスタルディスクマークの結果が以下です。

<img class="alignnone wp-image-539 size-medium" src="https://sumaho.tk/wp-content/uploads/2018/07/crucial_mx300_ahci002-300x274.png" alt="" width="300" height="274" srcset="https://sumaho.tk/wp-content/uploads/2018/07/crucial_mx300_ahci002-300x274.png 300w, https://sumaho.tk/wp-content/uploads/2018/07/crucial_mx300_ahci002.png 402w" sizes="(max-width: 300px) 100vw, 300px" />

全体的にレスポンスは向上しています。これはオマケの参考情報です。

### **追記 2019/10/18**  
このエラーが発生する状況は、以下が肝になる  

  1. Windowsのデバイスドライバーの設定（IDEかAHCI)   
  1. Windowsのレジストリーの情報で該当する項目の値（0かそれ以外か)   
  1. BIOS(EFI)の設定でSATAの接続設定（IDEかAHCI)    
  
上記の1と2に関しては予め設定しておく事。 
下記画像の様にデバイスドライバーがAHCIになっていないとブルー画面は解消されません。  
IDEモードの場合は無理矢理でもSTAT/AHCIモードに変更する事が必要です。   
 
![デバイスドライバー一覧のIDE](/img/ahic_controlpanel.png)  

その上でBIOSの設定をAHCIに変更します。  
**上記の1と2の両方の条件を満たしていないと何時まで経ってもブルー画面から抜け出せません。**  
