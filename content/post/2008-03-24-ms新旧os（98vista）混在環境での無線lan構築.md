---
title: MS新旧OS（98,Vista）混在環境での無線LAN構築
author: スフィア
type: post
date: 2008-03-24T12:44:00+00:00
RelPermalink: /2008/03/ms新旧os（98vista）混在環境での無線lan構築/
aliases:
    - /2008/03/ms新旧os（98vista）混在環境での無線lan構築/
    - /post/2008/03/ms新旧os 98 vista 混在環境での無線lan構築/
categories:
  - Windows
tags:
  - Windows Vista
  - Windows98 SE
  - イーサネットコンバーター
---
姉の家で新しいパソコンを購入する事になりパソコン選びに一緒に行って欲しいと言われ近所の電気屋さんでWindowsVistaを搭載したSONYのVAIOを買った。

### 姉の要望
今まで使っていたエプソンのプリンターPM-A700と、Windows98SEを搭載したNECのデスクトップを無線LANで繋ぎたいとの要望を受けた。

### 姉の要望
今まで使っていたエプソンのプリンターPM-A700と、Windows98SEを搭載したNECのデスクトップを無線LANで繋ぎたいとの要望を受けた。
んーん！と唸ってしまいました。
プリンターはエプソンだから大丈夫だろう！という予想通りちゃんとWindowsVista用のドライバーが公開されていました。

#### 最大の難関
超古い仕様のWindows98SEと最新のOSであるWindowsVistaの同一ネットワーク内の共存を実現しセキュリティーも万全の体制を得られるルーターが無い事でした。
で、近所のPCショップに電話を掛け捲ってこの要望を解決出来るルーターセットを見つける事が出来ました。それがこの、バッファロー AirStation \IEEE802.11b/g\ <a target="_blank" href="https://www.amazon.co.jp/BUFFALO-%E3%83%8F%E3%82%A4%E3%83%91%E3%83%AF%E3%83%BC-%E7%84%A1%E7%B7%9ALAN%E3%83%AB%E3%83%BC%E3%82%BF%E3%83%BC-Station-WHR-HP-G300N/dp/B002LSIXLC/ref=sr_1_fkmr0_1?__mk_ja_JP=%E3%82%AB%E3%82%BF%E3%82%AB%E3%83%8A&amp;keywords=WHR-HP-G54%2FEK&amp;qid=1570322371&amp;sr=8-1-fkmr0&_encoding=UTF8&tag=pasokon-news-22&linkCode=ur2&linkId=f5d74c7be152a29b6c0815b085df022e&camp=247&creative=1211">WHR-HP-G54/EK</a><img src="//ir-jp.amazon-adsystem.com/e/ir?t=pasokon-news-22&l=ur2&o=9" width="1" height="1" border="0" alt="" style="border:none !important; margin:0px !important;" />です。

#### 仕組み
灰色のルーターがメインのルータでここに有線のLANや無線LANを上位OSから繋ぎにいきます。つまり今回で言えばVistaから無線LANでこのルーターに繋げます。
で、問題のWindows98SEはもう一つのイーサネットコンバーターに有線で繋ぎます。これはWindows98SEのマシンからUSBタイプのLANコネクターを付けてそのLAN線をイーサネットコンバーターに繋ぐと言う意味です。
これにより親のルーターから見たWindows98SEのマシンはセキュリティー的にもイーサネットコンバーターのセキュリティレベルが保証されますのでieee802.11gや11aの規格に則った接続が出来るのです。

**なんだよ！無線LANじゃないじゃん！**

で、近所のPCショップに電話を掛け捲ってこの要望を解決出来るルーターセットを見つける事が出来ました。それがこの、バッファロー AirStation \IEEE802.11b/g\ <a target="_blank" href="https://www.amazon.co.jp/BUFFALO-%E3%83%8F%E3%82%A4%E3%83%91%E3%83%AF%E3%83%BC-%E7%84%A1%E7%B7%9ALAN%E3%83%AB%E3%83%BC%E3%82%BF%E3%83%BC-Station-WHR-HP-G300N/dp/B002LSIXLC/ref=sr_1_fkmr0_1?__mk_ja_JP=%E3%82%AB%E3%82%BF%E3%82%AB%E3%83%8A&amp;keywords=WHR-HP-G54%2FEK&amp;qid=1570322371&amp;sr=8-1-fkmr0&_encoding=UTF8&tag=pasokon-news-22&linkCode=ur2&linkId=f5d74c7be152a29b6c0815b085df022e&camp=247&creative=1211">WHR-HP-G54/EK</a><img src="//ir-jp.amazon-adsystem.com/e/ir?t=pasokon-news-22&l=ur2&o=9" width="1" height="1" border="0" alt="" style="border:none !important; margin:0px !important;" />です。
  

#### 仕組み
灰色のルーターがメインのルータでここに有線のLANや無線LANを上位OSから繋ぎにいきます。つまり今回で言えばVistaから無線LANでこのルーターに繋げます。

で、問題のWindows98SEはもう一つのイーサネットコンバーターに有線で繋ぎます。これはWindows98SEのマシンからUSBタイプのLANコネクターを付けてそのLAN線をイーサネットコンバーターに繋ぐと言う意味です。

これにより親のルーターから見たWindows98SEのマシンはセキュリティー的にもイーサネットコンバーターのセキュリティレベルが保証されますのでieee802.11gや11aの規格に則った接続が出来るのです。

**なんだよ！無線LANじゃないじゃん！**

たっ...確かに無線LANじゃないですね（汗）

でも、ルーターはCATVやFFTHやADSLの線が届いている1階に設置し、無線LANで使う機器は殆どが２階という現代の家の構造（勝手につくるな！）においては２階で有線であったにしてもそのイーサネットコンバーターが無線LANの代わりをしてくれるのですから事実上は無線LANの環境と呼べると思います。
Windows98SEとWindowsVistaが同一のネットワークで無線LAN、しかもセキュリティーレベルを守りながらっていう要望は基本的には絶対に無理なんです。でも、それを実現する為にこの様なイーサネットコンバーターを利用する方法もあります。この場合の選択としてベストではないかと思っています。

#### ポイント
最後に一つ私がとても苦労した部分をポイントとして挙げておきます。
イーサネットコンバーターと各種コードやPCの接続は添付の説明書通りに行ってください。手順は１から10まで手順書通りに進める事が一番大切です。

これを守らないと私の様に何時間も唸る事になります。
概要をお話すると、最初はPCの電源をOFFにしておき、USBケーブルは外しておく。つまり**イーサネットコンバーターと親機であるルーターとの接続が確立されるまで5分待とうが10分待とうが黙って待つ事が大事**です。

#### 概要

最初はPCの電源をOFFにしておき、USBケーブルは外しておく。つまり**イーサネットコンバーターと親機であるルーターとの接続が確立されるまで5分待とうが10分待とうが黙って待つ事が大事**です。

イーサネットコンバーターが親機と接続されてから手順書に従いケーブルを接続し、電源を入れるといった流れです。
