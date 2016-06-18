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

* *要素を調査*
* Webコンソール

# 要素を調査

* DOMを調べる
  * 要素(element)があるか
  * 属性(attribute)があるか

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

* ~~要素を調査~~
* *Webコンソール*

# Webコンソール

* JavaScriptのログ
  * console.log
* JavaScriptのコードを実行して試すこともできる

# Webコンソール

デモ

# サーバー

* *ネットワークモニター*
* Webサーバーのログ
* アプリケーションサーバーのログ

# ネットワークモニター

* ...

# ネットワークモニター

デモ

# Webサーバーのログ

* Railsとか

# アプリケーションサーバーのログ

* ...

# おまけ

法人向けFirefoxサポートで得た知見

# おまけ

* DOM Inspector
* ブラウザツールボックス

# DOM Inspector

* ...

# DOM Inspector

デモ

# ブラウザツールボックス

* ...

# ブラウザツールボックス

デモ
