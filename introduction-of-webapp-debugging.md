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

# クライアント

* 要素を調査
* Webコンソール
* ネットワークモニター

# サーバー

* Webサーバーのログ
  * Apache、nginx
* アプリケーションサーバーのログ
  * Unicorn、Puma

# クライアント

* *インスペクタ*
* Webコンソール
* *ネットワークモニター*

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
* ネットワークモニター

# Webコンソール

* JavaScriptなどのログを記録
  * console.log
* JavaScriptのコードを実行してWebページと対話

{::note} https://developer.mozilla.org/ja/docs/Tools/Web_Console {:/note}

# Webコンソール

デモ

# クライアント

* ~~インスペクタ~~
* ~~Webコンソール~~
* *ネットワークモニター*

# ネットワークモニター

* ネットワークリクエストの詳細を表示
  * HTTPステータス
  * リクエスト/レスポンス

{::note} https://developer.mozilla.org/ja/docs/Tools/Network_Monitor {:/note}

# ネットワークモニター

デモ

# 原因を切り分ける

* どこのエラーか
  * クライアント
  * サーバー
  * ネットワーク

# 原因を切り分ける

* クライアント側にエラーはないか
* サーバー側にエラーはないか
* サーバーに届いているか

# クライアント側にエラーはないか

* JavaScriptにログを仕込む
* Webコンソールを確認

# クライアント側にエラーはないか

* エラーある
  * クライアントが原因
* エラーない
  * 次へ

# サーバー側にエラーはないか

* Sinatraにログを仕込む
* アプリケーションサーバーのログを確認

# サーバー側にエラーはないか

* エラーある
  * サーバーが原因
* エラーない
  * 次へ

# サーバーに届いているか

* ネットワークモニターに表示されているか
* Webサーバーのログに表示されているか

# サーバーに届いているか

* 表示されていない
  * ネットワークが原因っぽい
* 表示されている
  * 次へ

# レスポンスが返ってきているか

* ネットワークモニターにレスポンスが表示されているか

# レスポンスが返ってきているか

* 返ってきていない
  * →サーバーが原因っぽい
* 返ってきている

# まとめ

* 標準ツールが充実
* クライアントかサーバーか切り分ける
