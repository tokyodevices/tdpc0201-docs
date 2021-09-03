# 使い方

## 接続方法

1. マザーボードのリセットボタン用ピンと、リセットマスターの出力ピンを接続します。(+と-の極性があります)
   リセットマスターと並列して手動のリセットボタンも使いたい方は、並列接続ピンにリセットボタンを接続します。

2. USBケーブルでリセットマスターとPC本体と接続します。

3. PCを起動します。

4. リセットマスターがリセットを実行しないよう、制御コマンドで内蔵カウンタをクリアしつづけます。

## 制御コマンド

[汎用制御コマンドTD-USB](https://github.com/tokyodevices/td-usb/blob/master/README_ja.md)を使用します。

Windows環境の場合には[TD-USBのページ](https://github.com/tokyodevices/td-usb/blob/master/README_ja.md)よりダウンロードしてください。
Linux環境の場合には、Githubの[tokyodevices/td-usbリポジトリ](https://github.com/tokyodevices/td-usb)からソースコードを取得し、お使いの環境向けにコンパイルしてください。


WindowsやLinuxのコマンドラインから下記を実行すると、リセットマスターをゼロクリアします。
お使いのPC環境から、定期的にこのコマンドを実行するようにしてください。

    > td-usb tcpc0201 set
