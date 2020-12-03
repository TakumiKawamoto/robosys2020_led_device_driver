# robosys2020_led_device_driver
ロボットシステム学　課題1　デバイスドライバ

# 内容


# 実験器具

- Raspberry Pi4 Model B
- LED（赤）x3, （緑）x3
- 抵抗 330Ω x3, 20Ω x1, 47Ω x1, 51Ω x1
- ブレッドボード
- 配線コード
- ジャンプワイヤ


<img src="https://github.com/TakumiKawamoto/robosys_led/blob/main/contents/IMG_20201203_172423.jpg" width="600px">

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

# 実演動画
