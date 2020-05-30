---
title: HDDを換装してSSD(crucial)が認識されない。フォーマットできない
author: スフィア
type: post
date: 2018-07-19T12:13:20+00:00
RelPermalink: /2018/07/hddを換装してssdにする時にssdが認識されない。初期化/
image: /wp-content/uploads/2018/07/illustrain06-biji03-246x200.png
aliases:
    - /2018/07/hddを換装してssdにする時にssdが認識されない。初期化/
    - /post/2018/07/hddを換装してssdにする時にssdが認識されない。初期化/

categories:
  - ハードウェア
  - パソコン

---
購入したCrucialなどのSSDが認識しない時には以下を確認してみて下さいね。(ssdはフォーマットする前に新しいディスクの追加操作が必要です）

ですので、改めて**「ssd フォーマット ソフト」**の様なものは必要ありません。Windowsの標準の機能で対応可能となります。

&nbsp;

<span class="green b">Windowsの例でご説明致します。</span>

<span class="green b"><span class="green b">Windowsのスタートメニューアイコン上で右クリック->ディスクの管理</span>を選んで下さい。</span>

<span class="blue b">（若しくは、「Windowsキー + R を同時に押して、ファイル名を指定して実行」のプログラムを表示させて、入力エリアに「diskmgmt.msc」と打ちOKボタンを押します。）</span>

&nbsp;

<img class="alignnone wp-image-485" src="https://sumaho.tk/wp-content/uploads/2018/07/win1.png" alt="" width="388" height="754" />

&nbsp;

そうすると<span class="red b">「新しいディスクが検出されました」</span>というダイアログが現れて、フォーマットする際のパーティーションの形式をどうするか聞いてきます。

&nbsp;

## MBR or GPT

MBR or GPT の選択を迫られます。

<img class="alignnone wp-image-291" src="https://sumaho.tk/wp-content/uploads/2018/06/new_disk.png" alt="" width="518" height="401" />

&nbsp;

<div class="chat_l ">
  <div class="talker">
    <b><img class="square" src="https://sumaho.tk/wp-content/uploads/2018/06/nacky1-150x150.jpg" alt="ナッキー" /> </b>
  </div>
  
  <div class="bubble_wrap">
    <div class="bubble" style="background-color:#cef2ae">
      <div class="bubble_in" style="border-color:#cef2ae">
        <p>
          よくわからない場合はMBRを選んで下さい。MBRはWindowsVISTA以前の形式にも対応する新旧どの環境でも使えるパーティション形式です。
        </p>
      </div>
    </div>
  </div>
</div>

GPTはWindowsVista以降のOSでしか使えない上に、BIOS(Windows起動前に、パソコンを立ち上げて最初に色々と文字を表示する基本OS）が対応していないと使えません。

なので、特別な理由（起動パーティーションを4つ以上欲しいとか、2TB以上の大きなSSDを使うとか）がない限りがMBRを選択しましょう。