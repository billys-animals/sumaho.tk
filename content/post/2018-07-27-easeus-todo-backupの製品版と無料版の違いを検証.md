---
title: EaseUS Todo Backupの製品版と無料版の違いを検証
author: スフィア
type: post
date: 2018-07-27T09:49:09+00:00
RelPermalink: /2018/07/easeus-todo-backupの製品版と無料版の違いを検証/
image: /wp-content/uploads/2018/07/clone1-246x200.png
category_relation:
  - 'y'
tag_relation:
  - 'y'
disp_description_relation:
  - 'n'
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
tw_card:
  - def
page_layout:
  - def
toc:
  - def
primary_category:
  - 128
page_meta_keyword:
  - easeus todo backup システムクローン クローン 違い,hdd ssd クローン 容量違い
pvc_views:
  - 1081
ampforwp-amp-on-off:
  - default
ampforwp-redirection-on-off:
  - enable
categories:
  - ソフトウエア
  - ハードウェア

---
EaseUS Todo Backup には2つのエディションがあります。

  1. Home 11.0
  2. <a href="https://jp.easeus.com/backup-software/free.html" target="_blank" rel="noopener">FREE</a>

機能的には全く同じなのですが、1は有料版の30日限定利用なので30日間は試用期間として有料版と同じ事が同じパフォーマンスで可能です。また、バックアップ機能は試していないのでこの時点で全く同じ事が出来る確証はありません

2は無料版なので30日制限等の縛りはありませんし、機能も同等なのですが、バックアップやリストアの速度があまり速くない様です。

## 両者の速度を試した結果

  1. 1のトライアルで230ＧＢのSSDから160GBのHDDにシステムクローンを試したところおよそ89分かかりました。
  2. 2のＦＲＥＥで、128GBのSSDから160GBのHDDにシステムクローンを試したところおよそ220分かかりました。

この事から、<span class="green b">製品版とＦＲＥＥ版のスピードの差は約2.5倍</span>という結果になりました。

### 実際にどちらのエディションを選ぶべきか？

SSDへの換装などでⅠ回限りの利用の場合には1のトライアル30日試用の製品版を選びましょう。

それ以外に少々遅くても日常的なバックアップ等興味がある人はFREEを選ぶと良いと思います。遅くても機能はきちんと使えます。

## クローン作成について

今回、はじめてEaseUS Todo Backup を使ったディスクのクローンを作成してみました。

### easeus todo backup システムクローンとクローンの違いとは何？

#### システムクローンとは

対象のドライブに複数のパーティションがあってそれを丸ごと、全てのパーティションをディスクごと複製するのがシステムクローン

##### システムクローンを作成する際に注意する事

クローン元のディスクの容量 <= クローン先のディスクの容量

#### クローンとは

対象のドライブに複数のパーティションがあってその中から起動パーティションなど（複数パーティションの全てではない）を複製するのがクローン

##### クローンを作成する際に注意する事

<span class="orange b">クローン元のディスク内の対象パーティションの実データの使用容量</span>  <= クローン先のディスクの全容量

これも成り立ちます。

容量の大きなHDDを容量の小さいSSDのクローンを作りたい場合にはこちらの機能を使います。
  
（クローン元で使用している実データ容量以上の容量が、クローン先に確保されていないと当然ダメです。）

<span class="green b">例えば、クローン元のディスクに、起動のCドライブ＋レカバリー領域のパーティション＋メーカー独自のシステム領域など存在していて、新しい環境のSSDではCドライブのみを容量の小さいSSDで運用した場合などにはこちらのクローンを利用します。</span>

<span class="a8ad 1q0aR9M-g7-qZE7VaO"></span>
  
<a href="https://px.a8.net/svt/ejp?a8mat=1C00JO+DSKUD6+1NCY+HUKPU&#038;a8ejpredirect=https%3A%2F%2Fpcshop.vector.co.jp%2Fservice%2Fservlet%2FCatalogue.Detail.Top%3FITEM_NO%3DSR437221" target="_blank" rel="nofollow">EaseUS Todo Backup 11.5</a>
  
<img border="0" width="1" height="1" src="https://www16.a8.net/0.gif?a8mat=1C00JO+DSKUD6+1NCY+HUKPU" alt="" />

&nbsp;

**※ここでのシステムクローンやクローンの定義はEaseUS Todo Backup内の機能のみで成り立つ意味で、一般的な言葉で現す表現とは異なります※**

&nbsp;

### 良かった点

  1. 作業時間が1時間30分足らずというのは過去に試したクローンツールの中では最速です
  2. 操作は非常に分かり易いものでした。
  3. SSDへの最適化モードや不良セクタをきちんと修正しながらクローンを作るオプションがとても嬉しい
  4. GUIで作業が完結するのでとても分かり易い

&nbsp;

### 悪かった点

  1. <del datetime="2018-07-29T03:40:07+00:00">クローン元よりもクローン先の方がディスク容量が小さいと処理そのものが出来ない。自動的に環境に合わせてくれるとありがたい。</del>
  2. クローンとシステムクローンとか、バックアップにも複数の名前があり、非常に分かり難い。メインメニューはもっとシンプルにした方が良い。

&nbsp;