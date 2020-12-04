# robosys2020_led_device_driver
ロボットシステム学　課題1　デバイスドライバ

# 内容

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

Raspberry Pi4 GPIOピン[21, 16, 25, 12]を使用

<img src="https://github.com/TakumiKawamoto/robosys_led/blob/main/contents/Circuit_image.jpg" width="320px"><img src="https://github.com/TakumiKawamoto/robosys_led/blob/main/contents/IMG_20201203_172423.jpg" width="580px">

# 実行方法

    $ git clone https://github.com/TakumiKawamoto/robosys_led.git
    $ cd robosys_led
    $ make
    $ sudo insmod myled.ko
    $ sudo chmod 666 /dev/myled0

# 操作方法

- レースシグナルカウントスタート

        $ echo s > /dev/myled0

- シグナル消灯

        $ echo 0 > /dev/myled0

- エラー表示

        $ echo t > /dev/myled0

# 実演動画
