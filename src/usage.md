# 使い方

## 接続方法


<img src="https://s3.ap-northeast-1.amazonaws.com/docs.tokyodevices.jp/tdpc0201-docs/TDPC0201_connection.png" />


1. 上記の接続図を参照して、マザーボードのリセットボタン用ピンと、リセットマスターの出力ピンを接続します。(+と-の極性があります)
   リセットマスターと並列して手動のリセットボタンも使いたい方は、リセットボタンを接続します。

2. USBケーブルでリセットマスターとPC本体と接続します。

3. PCを起動します。

4. リセットマスターがリセットを実行しないよう、制御コマンドで内蔵カウンタをクリアしつづけます。

## 制御コマンドの入手

[汎用制御コマンドTD-USB](https://github.com/tokyodevices/td-usb/blob/master/README_ja.md)を使用します。

Windows環境の場合には[TD-USBのページ](https://github.com/tokyodevices/td-usb/blob/master/README_ja.md)よりダウンロードしてください。
Linux環境の場合には、Githubの[tokyodevices/td-usbリポジトリ](https://github.com/tokyodevices/td-usb)からソースコードを取得し、お使いの環境向けにコンパイルしてください。

## ゼロクリア

WindowsやLinuxのコマンドラインから下記を実行すると、リセットマスターをゼロクリアします。
お使いのPC環境から、定期的にこのコマンドを実行するようにしてください。

    > td-usb tdpc0201 set


## 最も簡単な運用バッチプログラムの作成

Windowsのメモ帳等で、以下の内容を書き込んだ watchdog_clear.bat というバッチファイルを用意してください。

    (インストールした場所)\td-usb tdpc0201 set --loop

このバッチファイルを実行すると、1秒ごとにリセットマスターをゼロクリアします。
PCがフリーズしてバッチファイルが動作できなくなった時にリブートが実行されます。

