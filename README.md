# robosys2020_led_device_driver
ロボットシステム学　課題1　デバイスドライバ

# 内容

ロボットシステム学の講義で作成したものを改変しました
赤と緑のLEDを用いてレースのスタートシグナルを再現
- デバイスファイルに's'を書き込むとカウントダウンスタート (START)
- '0'を書き込むとシグナルが消灯 (TURN OFF)
- 's ' 0'以外が書き込まれるとLEDでエラー表示 (ERROR)

# 実験器具

- Raspberry Pi4 Model B
- LED(赤)x3, (緑)x3
- 抵抗 330Ω x3, 51Ω x3
- ブレッドボード
- 配線コード
- ジャンプワイヤ

# 回路

Raspberry Pi4 GPIOピン[21, 16, 25, 12]を使用し、それぞれLEDに接続

GPIO12は並列にLEDを3つ接続

<img src="https://github.com/TakumiKawamoto/robosys_led/blob/main/contents/Circuit_image.jpg" width="364px"><img src="https://github.com/TakumiKawamoto/robosys_led/blob/main/contents/image.jpg" width="580px">

# 実行方法

    $ git clone https://github.com/TakumiKawamoto/robosys_led.git
    $ cd robosys_led
    $ make
    $ sudo insmod myled.ko
    $ sudo chmod 666 /dev/myled0

# 操作方法

- シグナルカウントスタート

        $ echo s > /dev/myled0

- シグナル消灯

        $ echo 0 > /dev/myled0

- エラー表示（s,0以外の文字、数字）

        $ echo t > /dev/myled0

# 実演動画

[![](https://img.youtube.com/vi/kS7PiFLpQug/0.jpg)](https://www.youtube.com/watch?v=kS7PiFLpQug)

# ライセンス

[GNU General Public License v3.0](https://github.com/TakumiKawamoto/robosys_led/blob/main/COPYING)
