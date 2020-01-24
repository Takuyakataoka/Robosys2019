# ロボットシステム学課題概要

16C1702　片岡拓也　千葉工業大学

# 課題1について

## やったこと
ロボットシステム学の講義で用いられたLEDを光らせるプログラムを参考にし，
入力した数字をｎとしたときに，ｎ秒の転倒をｎ回させるようにしました．

## 使用したもの
* Raspberry Pi Model 3B+

## ラズパイの環境構築
* raspbian、イメージファイル
　https://www.raspberrypi.org/downloads/noobs/

## 参考文献
* Raspberry Piのアドレスマップ
https://www.raspberrypi.org/app/uploads/2012/02/BCM2835-ARM-Peripherals.pdf
* 上田先生の講義用リポジトリ
https://github.com/ryuichiueda/robosys2018/blob/master/06_device_driver.md

## プログラムの使用方法
* 環境構築
```
$ git clone https://github.com/Takuyakataoka/Robosys2019.git
$ cd Robosys2019
$ make
$ sudo insmod myled.ko
$ sudo chmod 666 /dev/myled0
```
* 使用例
```
$ echo 1 > /dev/myled0 #1秒間の点灯を1回
$ echo 2 > /dev/myled0 #2秒間の点灯を2回
```
## 動画
https://youtu.be/vkGvjm-wJ_Q
