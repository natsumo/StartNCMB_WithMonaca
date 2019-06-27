name: inverse
layout: true
class: center, middle, inverse
---
# Monaca で　　　　　<br>mobile backend<br>　　　を使ってみよう
富士通クラウドテクノロジーズ株式会社

.right[<img src="readme-img/takano.png" alt="takano.png" width="150px">]

.footnote[
20190628
]

---
layout: true
class: center, middle, inverse_sub
---
## はじめに

.right[<img src="readme-img/takano.png" alt="takano.png" width="150px">]


---
layout: false
### 概要

とりあえず mobile backend を使ってみましょう。<br>そして、何ができるか実際に触って理解しましょう。

* 今日だけでも「データストア」を結構理解できます👍

#### 資料
https://natsumo.github.io/StartNCMB_WithMonaca


---
### アジェンダ

1. mobile backend って何？
1. mobile backend を手っ取り早く使うには
1. 実際に触ってみましょう①
  1. Monaca の準備
  1. Monaca の練習
  1. mobile backend の準備
  1. mobile backend と Monaca を連携する
  1. mobile backend にデータを保存する
1. 実際に触ってみましょう②
  1. mobile backend に保存したデータを取得する
1. まとめ

---
layout: true
class: center, middle, inverse_sub
---
## 1. mobile backend って何？

---
layout: false
### 1. mobile backend って何？

私たちが提供するサービス [ニフクラ mobile backend](https://mbaas.nifcloud.com/) とは何か？<br>
一言で言うなれば「 **構築不要ですぐに使えるクラウドデータベース** 」

.center[
<img src='readme-img/about_NCMB.png' alt='about_NCMB' width='400px'>
]

アプリに欲しい機能は大体用意されているので、使えさえすればこっちのもの。<br>
使うために必要なことは .font_color_remark[**使い方を覚える**] これだけ。

---
layout: true
class: center, middle, inverse_sub
---
## 2. mobile backend を手っ取り早く使うには

---
layout: false
### 2. mobile backend を手っ取り早く使うには

開発中のアプリがあればそれに組み込むのが一番。<br>（AndroidでもiOSでもUnityでも）

開発中のアプリが特に無くて、<br>
とりあえず使い勝手を試したいのであれば [Monaca](https://ja.monaca.io/) を使うと良い👌

.center[
<img src='readme-img/about_Monaca.png' alt='about_Monaca' width='400px'>
]

* 連携が断然楽
* 環境構築不要（ブラウザで開発）
* みんな知ってるJavaScript

などなど、簡単に使えるので。

今回はこの [Monaca](https://ja.monaca.io/) を使って mobile backend の使い方を習得していきましょう。

---
layout: true
class: center, middle, inverse_sub
---
## 3. 実際に触ってみましょう①

---
layout: false
### 3. 実際に触ってみましょう①

1. Monaca の準備
1. Monaca の練習
1. mobile backend の準備
1. mobile backend と Monaca を連携する
1. mobile backend にデータを保存する

---
#### 1. Monaca の準備

利用環境を準備する。

* ブラウザ
  * <a href='https://www.google.com/chrome/' target='_blank'>Chrome</a>以外では動きません
* アカウント
  * <a href='https://monaca.mobi/ja/signup' target='_blank'>Monaca 利用登録（無料）</a>
* デバッガー【任意】
  * <a href='https://ja.monaca.io/debugger.html' target='_blank'>Monacaデバッガー</a>

__ ★後で消す

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 1. Monaca の準備

Monaca にログインする。

.center[<img src="readme-img/Monaca00.png" alt="Monaca00.png" width="700px">]

<a href='https://ja.monaca.io/' target='_blank'>ja.monaca.io</a>

_★あとで消す_

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 1. Monaca の準備

Monaca プロジェクトを作ります。

.center[<img src="readme-img/Monaca01.png" alt="Monaca01.png" width="400px">]

「最小限のテンプレート」を選びます。

.center[<img src="readme-img/Monaca02.png" alt="Monaca02.png" width="650px">]

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 1. Monaca の準備

プロジェクト名はこのままでOKです。「作成」をクリックします。

.center[<img src="readme-img/Monaca03.png" alt="Monaca03.png" width="500px">]



.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 1. Monaca の準備

プロジェクトが作成されます。

.center[<img src="readme-img/Monaca04.png" alt="Monaca04.png" width="350px">]

プロジェクトを選択すると、右側に表示される「クラウドIDEで開く」をクリックします。

.center[<img src="readme-img/Monaca05.png" alt="Monaca05.png" width="400px">]


.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 1. Monaca の準備

プロジェクトが開かれます。

.center[<img src="readme-img/Monaca06.png" alt="Monaca06.png" width="750px">]


.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 2. Monaca の練習

`index.html` が表示されています。 `body` タグ内を少し編集してみましょう。

.center[<img src="readme-img/Monaca10.png" alt="Monaca10.png" width="750px">]

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 2. Monaca の練習

一度消して、何か書いてみましょう。

.center[<img src="readme-img/Monaca11.png" alt="Monaca11.png" width="750px">]

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 2. Monaca の練習
書けたら保存します。<br>
「ファイル」＞「保存」でプロジェクトを保存します。

.center[<img src="readme-img/Monaca12.png" alt="Monaca12.png" width="750px">]

それぞれ以下でも保存できます。
* Windows「Ctrl + s」
* Mac「command + s」

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 2. Monaca の練習

保存すると、右側プレビュー画面が更新され `body` タグ内に書いた文字が表示されます。

.center[<img src="readme-img/Monaca13.png" alt="Monaca13.png" width="750px">]

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 2. Monaca の練習

それではいよいよ本題に向けた練習に入ります。<br>
**mobile backend にデータが保存されるボタン** を作ってみましょう。

さっき書き換えた文字の下に `button` タグを用意します。

.center[<img src="readme-img/Monaca14.png" alt="Monaca14.png" width="650px">]

保存してプレビュー画面で確認しましょう。

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 2. Monaca の練習

ボタンにクリックイベントを追加しましょう。

.center[<img src="readme-img/Monaca15.png" alt="Monaca15.png" width="500px">]

<br><br>

**mobile backend にデータを保存する処理** を書く `function` 名を「 `addData()` 」としましょう。

.center[<img src="readme-img/Monaca16.png" alt="Monaca16.png" width="600px">]

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 2. Monaca の練習

**mobile backend にデータを保存する処理** を書く `function` 「 `addData()` 」を用意しましょう。JavaScriptなので、`script` タグ内に記述します。

.center[<img src="readme-img/Monaca17.png" alt="Monaca17.png" width="600px">]

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 2. Monaca の練習

一応動作確認をしておきましょう。<br>一旦 `alert` を表示する `function` にしましょう。

.center[<img src="readme-img/Monaca18.png" alt="Monaca18.png" width="600px">]


.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 2. Monaca の練習

保存してからプレビュー画面でボタンを押してみましょう。<br>
ブラウザの `alert` が表示されればOKです。

.center[<img src="readme-img/Monaca19.png" alt="Monaca19.png" width="730px">]

次の作業のために、 `alert` を消して保存しておきましょう。

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 3. mobile backend の準備

**mobile backend にデータが保存されるボタン** を作るために、ここからは mobile backend 側の準備をしていきましょう。まずはアカウントを用意します。「無料登録」をクリックします。

.center[<img src="readme-img/Monaca20.png" alt="Monaca20.png" width="730px">]

<a href='https://mbaas.nifcloud.com/' target='_blank'>mbaas.nifcloud.com</a>

_★あとで消す_

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 3. mobile backend の準備

**無料** で利用するには SNSアカウント で会員登録を行います。

.center[<img src="readme-img/Monaca21.png" alt="Monaca21.png" width="600px">]

利用可能なSNSアカウント
* Facebook
* Twitter
* Google (Gmail)

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 3. mobile backend の準備


.center[<img src="readme-img/Monaca22.png" alt="Monaca22.png" width="400px">]

.size_small_7[
＜いずれのアカウントも所持していない場合＞<br>いずれも無料で作成可能ですが、Googleアカウント（Gmail）がおすすめです。<br><a href='https://accounts.google.com/signup' target='_blank'>Googleアカウントの作成</a>
]

_★あとで消す_


.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 3. mobile backend の準備

認証処理が完了すると、メールアドレスの登録画面が表示されます。メールアドレスを入力して「確認メールを送信」をクリックします。

.center[<img src="readme-img/Monaca23.png" alt="Monaca23.png" width="400px">]

確認メールが届くので指示に従って会員登録を進めてください。

.size_small_7[
※このメールアドレスはSNSアカウントとは別に、自由に設定できます。
]

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 3. mobile backend の準備

会員登録が完了したらログインをします。

.center[<img src="readme-img/Monaca30.png" alt="Monaca30.png" width="750px">]

<a href='https://mbaas.nifcloud.com/' target='_blank'>mbaas.nifcloud.com</a>

_★あとで消す_

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 3. mobile backend の準備

会員登録をする際に使用した SNSアカウント を選択します。

.center[<img src="readme-img/Monaca31.png" alt="Monaca31.png" width="400px">]

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 3. mobile backend の準備

初回のみ利用規約に同意が必要です。内容を確認したらチェックを入れ、 「アカウント登録」をクリックします。

.center[<img src="readme-img/Monaca32.png" alt="Monaca32.png" width="400px">]

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 3. mobile backend の準備

ログインが完了すると、「アプリの新規作成」画面が表示されます。作成するアプリ単位で、mobile backend 上にもアプリを作成します。<br>「TestApp」と入力して、「新規作成」をクリックしましょう。

.center[<img src="readme-img/Monaca33.png" alt="Monaca33.png" width="400px">]

.left-column[
.size_small_7[
.right[
＜利用がはじめてではない場合＞<br>既にアプリを作成している場合は、<br>改めてアプリを作成します。
]
]
]

.right-column[
<img src="readme-img/Monaca34.png" alt="Monaca34.png" width="100px">
]

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 3. mobile backend の準備

アプリが作成されると、 **APIキー** が発行されます。後ほど使用します。一旦「OK」をクリックして画面を閉じます。

.center[<img src="readme-img/Monaca35.png" alt="Monaca35.png" width="400px">]

.size_small_7[
（参考）APIキーは２種類
* アプリケーションキー
  * アプリを特定するためのキー（ユニークキー）
* クライアントキー
  * 認証キー
]

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 3. mobile backend の準備

管理画面のダッシュボードが表示されます。

.center[<img src="readme-img/Monaca36.png" alt="Monaca36.png" width="750px">]

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 3. mobile backend の準備

文字列データは「データストア」に保存されます。（この後使っていきます。）

.center[<img src="readme-img/Monaca37.png" alt="Monaca37.png" width="750px">]

.size_small_7[
（参考）デフォルトクラス：
* installation
  * プッシュ通知配信端末情報が格納されるクラス
* role
  * 会員管理で設定した会員グループが格納されるクラス
]

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 4. mobile backend と Monaca を連携する

いよいよ **mobile backend にデータを保存する処理** を実装していきます。<br>
Monaca に戻って、図の手順で実装していきます。

.center[<img src="readme-img/Monaca40.png" alt="Monaca40.png" width="750px">]

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 4. mobile backend と Monaca を連携する
##### 4.1. mobile backend のSDKを導入する（コンポーネントの追加）

「設定」＞「JS/CSSコンポーネントの追加と削除」をクリックします。

.center[<img src="readme-img/add_sdk01.png" alt="add_sdk01.png" width="230px">]


.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 4. mobile backend と Monaca を連携する
##### 4.1. mobile backend のSDKを導入する（コンポーネントの追加）

「コンポーネント名」に「 **ncmb** 」と入力して「検索する」をクリックします。

.center[<img src="readme-img/add_sdk02.png" alt="add_sdk02.png" width="700px">]


.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 4. mobile backend と Monaca を連携する
##### 4.1. mobile backend のSDKを導入する（コンポーネントの追加）

mobile backend のSDK「ncmb」が表示されるので「追加」をクリックします。

.center[<img src="readme-img/add_sdk03.png" alt="add_sdk03.png" width="700px">]


.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 4. mobile backend と Monaca を連携する
##### 4.1. mobile backend のSDKを導入する（コンポーネントの追加）

バージョンはそのままで、「インストール」をクリックします。

.center[<img src="readme-img/add_sdk04.png" alt="add_sdk04.png" width="600px">]


.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 4. mobile backend と Monaca を連携する
##### 4.1. mobile backend のSDKを導入する（コンポーネントの追加）

必ずチェックボックスにチェックを入れてください。「保存」をクリックします。

.center[<img src="readme-img/add_sdk05.png" alt="add_sdk05.png" width="500px">]


.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 4. mobile backend と Monaca を連携する
##### 4.1. mobile backend のSDKを導入する（コンポーネントの追加）

一覧に「ncmb」が表示されればSDK導入完了です。

.center[<img src="readme-img/add_sdk06.png" alt="add_sdk06.png" width="700px">]


.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 4. mobile backend と Monaca を連携する
##### 4.2. 導入したSDKを初期化する

SDKは使う前に必ず初期化をする必要があります。初期化には mobile backend でアプリ作成時に発行された  **APIキー** を使います。まずは変数としてAPIキーの置き場を用意しましょう。

.center[<img src="readme-img/Monaca41.png" alt="Monaca41.png" width="700px">]


.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 4. mobile backend と Monaca を連携する
##### 4.2. 導入したSDKを初期化する

mobile backend の管理画面を開いて、APIキーを確認します。APIキーは「アプリ設定」にあります。コピーボタンを使ってそれぞれ変数に代入しましょう。

.center[<img src="readme-img/Monaca42.png" alt="Monaca42.png" width="700px">]


.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]


---
#### 4. mobile backend と Monaca を連携する
##### 4.2. 導入したSDKを初期化する

貼り付け終わるとこんな感じです。

.center[<img src="readme-img/Monaca43.png" alt="Monaca43.png" width="750px">]


.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]


---
#### 4. mobile backend と Monaca を連携する
##### 4.2. 導入したSDKを初期化する

APIキーを引数に設定して以下のように書くとSDKが初期化されます。

.center[<img src="readme-img/Monaca44.png" alt="Monaca44.png" width="750px">]

.size_small_7[
（参考）4.1. と 4.2. は mobile backend を使う際、必ず必要な作業です。覚えておきましょう。
]

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]


---
#### 5. mobile backend にデータを保存する
##### 5.1. mobile backend に「Hello, NCMB!」と保存する

連携ができたので、あとは保存のコードを `addData()` メソッド内に記述していきます。

.center[<img src="readme-img/Monaca50.png" alt="Monaca50.png" width="700px">]

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 5. mobile backend にデータを保存する
##### 5.1. mobile backend に「Hello, NCMB!」と保存する

保存先クラスを作ります。クラス名は「TestClass」としておきましょう。

.center[<img src="readme-img/Monaca51.png" alt="Monaca51.png" width="700px">]



.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 5. mobile backend にデータを保存する
##### 5.1. mobile backend に「Hello, NCMB!」と保存する

クラスのインスタンスを生成します。

.center[<img src="readme-img/Monaca52.png" alt="Monaca52.png" width="680px">]

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 5. mobile backend にデータを保存する
##### 5.1. mobile backend に「Hello, NCMB!」と保存する

インスタンスに値をセットします。フィールド名を「message」、値を「Hello, NCMB!」としましょう。

.center[<img src="readme-img/Monaca53.png" alt="Monaca53.png" width="680px">]

* `.set('key', 'value')` ：値の設定
  * key: フィールド名
  * value: 値

.size_small_7[
（参考）クラス名やフィールド名について<br>
クラス名／フィールド名は無ければ新規作成してくれるし、既に存在しているならば既存のクラス／フィールドを指定してくれます。（存在有無を気にする必要がないので楽ですね👏）
]

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 5. mobile backend にデータを保存する
##### 5.1. mobile backend に「Hello, NCMB!」と保存する

値を設定したら保存します。JavaScriptなので、メソッドチェーンで書けます。

.center[<img src="readme-img/Monaca54.png" alt="Monaca54.png" width="680px">]

* `.save()` ：保存

実装は以上です。

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 5. mobile backend にデータを保存する
##### 5.1. mobile backend に「Hello, NCMB!」と保存する

動作確認をしてみましょう。プロジェクトを保存して、プレビュー画面からボタンを押してみましょう。

.center[<img src="readme-img/Monaca55.png" alt="Monaca55.png" width="750px">]

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
#### 5. mobile backend にデータを保存する
##### 5.1. mobile backend に「Hello, NCMB!」と保存する

mobile backend 上に正しくデータが保存されたか確認してみましょう。<br>「データストア」を開くと、新しく「TestClass」ができています。クリックすると保存されたデータが確認できます。

.center[<img src="readme-img/Monaca56.png" alt="Monaca56.png" width="700px">]

.size_small_7[
（TRY）Monacaのプレビュー画面に戻ってボタンを何度か押してから改めて TestClass を確認してみましょう😘
]

.right_under[
.size_small_7[
.font_color_ncmb_blue[
3.実際に触ってみましょう①
]
]
]

---
layout: true
class: center, middle, inverse_sub
---
## 4. 実際に触ってみましょう②

---
layout: false
### 4. 実際に触ってみましょう②

1. mobile backend に保存したデータを取得する

ボタンを押すと「今何件 mobile backend 上にデータが保存されているか」を取得して画面に表示するようにしてみましょう👀

---
#### 1. mobile backend に保存したデータを取得する

`body` タグ内に新しいボタンと取得した件数を表示するための `div` タグを用意しましょう。ボタンが押されたら呼び出される `function` 名は「 `countData()` 」としましょう。また、 `div` タグには `id` を付けておきましょう。「 `counter` 」としましょう。

.center[<img src="readme-img/Monaca60.png" alt="Monaca60.png" width="600px">]


.right_under[
.size_small_7[
.font_color_ncmb_blue[
4.実際に触ってみましょう②
]
]
]

---
#### 1. mobile backend に保存したデータを取得する

**mobile backend に保存したデータの件数を取得する処理** を書く `function` 「 `countData()` 」を用意しましょう。

.center[<img src="readme-img/Monaca61.png" alt="Monaca61.png" width="750px">]

.right_under[
.size_small_7[
.font_color_ncmb_blue[
4.実際に触ってみましょう②
]
]
]

---
#### 1. mobile backend に保存したデータを取得する

**mobile backend に保存したデータの件数を取得する処理** を実装していきます。保存先クラスの指定をしますが、 3.5.1.でデータを保存したクラスと同じクラスを指定すればいいので、コードを共有します。 `function` の外に出してフィールド変数にします。

.center[<img src="readme-img/Monaca62.png" alt="Monaca62.png" width="750px">]


.right_under[
.size_small_7[
.font_color_ncmb_blue[
4.実際に触ってみましょう②
]
]
]

---
#### 1. mobile backend に保存したデータを取得する

データの取得は検索を行います。先に検索条件を設定します。件数を取得を指定します。

.center[<img src="readme-img/Monaca63.png" alt="Monaca63.png" width="600px">]

* `.count()`：件数を指定

.right_under[
.size_small_7[
.font_color_ncmb_blue[
4.実際に触ってみましょう②
]
]
]

---
#### 1. mobile backend に保存したデータを取得する

全件数を取得したいので、全件検索をします。

.center[<img src="readme-img/Monaca64.png" alt="Monaca64.png" width="600px">]

* `.fetchAll()`：全件検索処理

.right_under[
.size_small_7[
.font_color_ncmb_blue[
4.実際に触ってみましょう②
]
]
]

---
#### 1. mobile backend に保存したデータを取得する

コールバックを設定します。返り値をそれぞれ、成功時： `results` 、失敗時： `error` としましょう。

.center[<img src="readme-img/Monaca65.png" alt="Monaca65.png" width="600px">]

* `.then()`：検索成功時の処理
* `.catch()`：検索失敗時の処理

.right_under[
.size_small_7[
.font_color_ncmb_blue[
4.実際に触ってみましょう②
]
]
]

---
#### 1. mobile backend に保存したデータを取得する

検索取得に成功すると、返り値として件数の情報が取得できます。ここでは「`results.count`」で取得できます。変数化しておきましょう。

.center[<img src="readme-img/Monaca66.png" alt="Monaca66.png" width="580px">]

* 返り値 `.count` ：件数の取得

.right_under[
.size_small_7[
.font_color_ncmb_blue[
4.実際に触ってみましょう②
]
]
]

---
#### 1. mobile backend に保存したデータを取得する

先ほど作った `div` タグに件数を表示しましょう。

.center[<img src="readme-img/Monaca67.png" alt="Monaca67.png" width="650px">]


.right_under[
.size_small_7[
.font_color_ncmb_blue[
4.実際に触ってみましょう②
]
]
]

---
#### 1. mobile backend に保存したデータを取得する

（参考）検索処理失敗時は `alert` でエラーを表示するようにしておくと便利です☝️

.center[<img src="readme-img/Monaca68.png" alt="Monaca68.png" width="650px">]


.right_under[
.size_small_7[
.font_color_ncmb_blue[
4.実際に触ってみましょう②
]
]
]

---
#### 1. mobile backend に保存したデータを取得する

動作確認をしてみましょう。プロジェクトを保存して、プレビュー画面からボタンを押してみましょう。

.center[<img src="readme-img/Monaca69.png" alt="Monaca69.png" width="700px">]


.right_under[
.size_small_7[
.font_color_ncmb_blue[
4.実際に触ってみましょう②
]
]
]

---
#### 1. mobile backend に保存したデータを取得する

件数が表示されれば取得成功です！mobile backend の管理画面を確認して、実際の件数と一致しているか確認してみましょう😄

.center[<img src="readme-img/Monaca70.png" alt="Monaca70.png" width="200px">]

.size_small_7[
（TRY）最初に作ったボタンを何回か押してから、取得するボタンを押してみましょう。件数の変化がわかります😉
]


.right_under[
.size_small_7[
.font_color_ncmb_blue[
4.実際に触ってみましょう②
]
]
]

---
layout: true
class: center, middle, inverse_sub
---
## まとめ

---
layout: false

### まとめ

お疲れ様でした💪<br><br>短い時間のセミナーですが、mobile backen の使い方の基本が理解いただけたのではないかなと思います。<br><br>本セミナーの内容は参考書「 .font_color_ncmb_blue[**Monaca と ニフクラ mobile backend で学ぶ はじめてのプログラミング ～クラウド連携アプリ開発編～**] 」にも掲載している内容です。「mobile backend ってどんな感じで使えるサービスなんだろう？」という疑問を解消して、参考書を開いていただくための足掛かりになれれば幸いです🙏<br><br>ぜひ皆様のアプリ開発に mobile backend をお役立てください👍👍
