# Webアプリデバッグ入門

author
:   Masafumi Yokoyama

content-source
:   勉強会@Sinatra札幌

date
:   2016-06-19

allotted-time
:   40m

theme
:   nyankosakana

# デバッグとは

* バグを見つける
* バグを直す

# デバッグとは

* *バグを見つける*
* バグを直す

# バグを見つける

* デバッグツール

# デバッグツール

* Firefox/Google Chrome標準添付
  * F12で出てくるやつ
  * 標準添付のツールが充実してきたので、Live HTTP HeadersやHttpFox、Findbugsなどは不要になってきている

# バグを見つける

* どちらのエラーか
  * クライアント
  * サーバー

# クライアント

* 要素を調査
* Webコンソール

# サーバー

* ネットワークモニター
* Webサーバーのログ
* アプリケーションサーバーのログ

# クライアント

* *インスペクタ*
* Webコンソール

# インスペクタ

* 要素を調査
* DOMを調べる
  * 要素(element)があるか
  * 属性(attribute)があるか

{::note} https://developer.mozilla.org/ja/docs/Tools/Page_Inspector {:/note}

# 要素

```html
<a href="..."></a>
```

# 属性

```html
href="..."
```

# 要素を調査

デモ

# クライアント

* ~~インスペクタ~~
* *Webコンソール*

# Webコンソール

* JavaScriptなどのログを記録
  * console.log
* JavaScriptのコードを実行してWebページと対話

{::note} https://developer.mozilla.org/ja/docs/Tools/Web_Console {:/note}

# Webコンソール

デモ

# サーバー

* *ネットワークモニター*
* Webサーバーのログ
* アプリケーションサーバーのログ

# ネットワークモニター

* ネットワークリクエストの詳細を表示
  * HTTPステータス
  * リクエスト/レスポンス

{::note} https://developer.mozilla.org/ja/docs/Tools/Network_Monitor {:/note}

# ネットワークモニター

デモ

# Webサーバーのログ

* Apache/nginx

# アプリケーションサーバーのログ

* Sinatra/Rails

# まとめ

* 標準ツールが充実
* クライアントかサーバーか切り分ける
