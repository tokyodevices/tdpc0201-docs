# デバイスの設定

TD-USBコマンドを使用してデバイスの設定を変更できます。

## リセットまでの秒数の変更

次の例では警告ブザーが鳴るまでの時間を300秒に, 警告ブザーが鳴ってからリセットが発生するまでの時間を10秒に変更します:

    > td-usb tdpc0201 set WATCHING_TIME=300
    > td-usb tdpc0201 set WARNING_TIME=10

デバイスの設定を変更し終わったら本体の不揮発目メモリに書き込みます(saveしないと電源OFFで設定が元に戻ります):

    > td-usb tdpc0201 save

## 警告時のブザーのオン・オフ

次の例ではブザーの鳴動をオフにします:

    > td-usb tdpc0201 set CONFIG_FLAG=0

次の例ではブザーの鳴動をオンにします:

    > td-usb tdpc0201 set CONFIG_FLAG=1

デバイスの設定を変更し終わったら本体の不揮発目メモリに書き込みます(saveしないと電源OFFで設定が元に戻ります):

    > td-usb tdpc0201 save

