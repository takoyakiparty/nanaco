# 七個

七個はnanacoギフトIDを登録します。  
複数のnanacoギフトIDを登録する際に本領発揮します。煩わしいページ遷移や大量の入力は七個が担います。

## 実行環境

| ＃ | 種類 | 名前 | 備考 |
|---|---|---|---|
|1|OS|Windows 10 or 11|Power Automateが稼働すれば他OSもおそらく可能|
|2|ブラウザ|Microsoft Edge|OS標準搭載。|
|3|アプリ|デスクトップ用 Power Automate |Win10は無料でインストール可能。<br>Win11なら標準搭載。|

## 準備

1. Edge設定で「www.nanaco-net.jp」に対する権限「ポップアップとリダイレクト」を許可する。<br>
![ポップアップ許可](https://takoyakiparty.github.io/nanaco/parts/popupkyoka.png)
1. Edgeに拡張機能「Microsoft Power Automate」をインストール&有効(オン)にする。<br>
[拡張機能紹介・設定ページ](https://microsoftedge.microsoft.com/addons/detail/microsoft-power-automate/njjljiblognghfjfpcdpdbpbfcmhgafg)
1. Power Automate
    1. Win10の場合、Power Automateをインストールする。<br>
    [インストール手順](https://docs.microsoft.com/ja-jp/power-automate/desktop-flows/install)
    1. Power Automateを起動し、Microsoftアカウントでサインインする。
    1. 「新しいフロー」を作成する。フロー名は「七個」とする。
    1. フロー「七個」の編集を選ぶ。編集ウィンドウが開く。
    1. 「新しいサブフロー」をサブフロー名「log」で作成し、次のテキスト内容を貼り付ける。<br>
    [logソース](https://raw.githubusercontent.com/takoyakiparty/nanaco/main/src/log.robin)
    1. Mainフローに次のテキスト内容を貼り付ける。<br>
    [Mainソース](https://raw.githubusercontent.com/takoyakiparty/nanaco/main/src/Main.robin)
    1. フローを保存する。
    1. フロー「七個」の編集ウィンドウを閉じる。

## 実行方法

1. Power Automateでフロー「七個」を実行する。
1. 次のダイアログが表示されるのでOKを押す。<br>
![ログインを求めるダイアログ](https://takoyakiparty.github.io/nanaco/parts/dialog1.png)
1. nanacoのサイトにnanaco番号等を入力しログインする。
1. 次のダイアログが表示されるので、登録するギフトIDを貼り付ける。複数のギフトIDは改行で区切る。<br>
![ギフトIDの入力を求めるダイアログ](https://takoyakiparty.github.io/nanaco/parts/dialog2.png)
1. OKを押す。
