#古いプロジェクトは百度の小さいゲームに似合います。

>author：charley

####いくつかの古いプロジェクトのために、小さなゲームのニーズがありますので、本編では、古いプロジェクトの適切な手順とリンクを詳しく紹介します。

**Tips:**文の中で3 Dプロジェクトの創建を始めとして、この篇が3 Dプロジェクトの適応だけであることを代表しません。本明細書では、適応案は2 Dと3 Dの両方に共通していますが、言語バージョンには少し違いがあります。

####必読のヒント:

>1、本文を読む前に、まず「百度のミニゲームを作成する」を読んでください。より多くの配置環境の基礎内容は本編では紹介しません。
>
>2、新しいミニゲームのアイテムは、直接的にミニゲームのサンプルアイテムを作成することをおすすめします。審査時に作成された通常のプロジェクトであれば、本編のミニゲームの適応プロセスを学び、適応することができます。



###第1ステップ：例となるアイテムを作成します。(既存の古いアイテムはこのステップをスキップできます。)

まずLayaAirIDEを開けて、新規プロジェクトインターフェースに入ります。LayaAir 3 Dサンプル項目を選択します。

>Tips：本ステップは、旧プロジェクトの適応プロセスを実証するために、わざと一般的な3 Dサンプルプロジェクトを作成する。
>

![图1](img/baidu3.png) 


プロジェクト名、パスを入力して、言語タイプとエンジンバージョンを選択してください。

>（基本的には流れが一致していますので、本編は各言語の開発者向けですが、TSプロジェクトの流れでスクリーンショットを行います。他の言語バージョンであれば、違いがあります。追加的に説明します。）

OKです。続けます。

作成をクリックすると、3 Dプロジェクトの作成が完了します。



###第二ステップ：百度のミニゲームに似合います。

####1、ミニゲームが似合う前提準備

エンジンとIDEは現在の最新のベータ版または安定版を使います。LayaAirIDEは1.8.0 betaバージョンから始まり、古いプロジェクトのワンタッチリリースをサポートします。だから古いバージョンIDEとエンジンライブラリでアップグレードしていません。先にアップグレードすることを忘れないでください。



####2、ミニゲームの適応ライブラリを参照する

#####TSとJSの適応方法

1.8.0 betaから、サンプルアイテムを作成すると、TSとJSアイテムが自動的にミニゲーム適応ライブラリJSに導入されます。`“libs/laya.wxmini.js”`をクリックします。

![图](img/baidu4.png) 


図中のコード:


```html

<!--提供了百度小游戏的适配-->
<script type="text/javascript" src="libs/laya.bdmini.js"></script>
```


1.8.0以前のTSやJSの古いプロジェクトであれば、開発者は`bin/index.html`の中で手動で図中の赤い枠の中のこのコードに参加して、また現在使っているのが1.8.0以降の新しいバージョンのエンジンライブラリであるかどうかを確認します。そうでないと、新しいエンジンライブラリに切り替えます。そうでないと、運行時にlaya.bdmini.jsが見つからないため、エラーが発生します。

#####AS 3プロジェクトの適応方法

AS 3プロジェクトは、1.8.0以降の新しいバージョンのエンジンライブラリを使用した後、開発者が入り口クラスに手動でこのコードを追加するだけで、すぐにゲームの適応ライブラリの導入を完了します。


```java

import laya.bd.mini.MiniAdapter;
```



####3、初期化ミニゲームの適応ライブラリ

古いプロジェクトは創立の時、プロジェクトの入り口で適応ライブラリを初期化していませんので、百度のゲームバージョンを成功的に発表することを保証するために、私達はゲームの入り口の内で適応ライブラリの初期化を行わなければなりません。

**Tips**:*Baiduの初期化は、初期化エンジンの前に必要です。*

#####TSとJSプロジェクトの適応方法は、下図のようになります。

![图](img/baidu5.png) 


TSまたはJS項目の適応コードは以下の通りです。


```typescript

//初始化小游戏适配库
Laya.BMiniAdapter.init();
```


#####AS 3プロジェクトの適合方法は下図の通りです。

![图](img/baidu6.png) 


図中のAS 3項目の適合コードは以下の通りです。


```java

//百度小游戏适配
BMiniAdpter.init(); 
```




####4、コンパイルコード

適合コードの追加を完了しました。コンパイルまたはデバッグボタン（F 5）をクリックして、エラーメッセージがなければ、3次元のキューブが見られます。

![图2](img/2.png) 


>Tips：ある程度のポイントを適応してコンパイルしたり、デバッグしたりしたら、適応コードは有効になりません。

実行デバッグのポップアップウィンドウを閉じます。ミニゲームの発表コーナーに入ることができます。

これで、ミニゲームの相性が完成しました。

簡単にまとめてみると、新版のエンジンを使った後、適応ライブラリを引用し、適応ライブラリを初期化するという二つの核心ステップです。やはり簡単です。

他のミニゲームのリリース、デバッグなどは新プロジェクトと共通しています。他の関連文書を見ることができます。

この文書に疑問があれば、公式サイトに質問してください。コミュニティの中のリンクを公式QQ群の中@管理人charleyに送ってもいいです。

コミュニティURL：https://ask.layabox.com/



##この文章は賞賛します

本論文があなたのために役立つと思ったら、スキャンコードの作者への賞賛を歓迎します。激励は私たちがより多くの優れた文書を書くための動力です。

![wechatPay](../../../wechatPay.jpg)