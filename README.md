[日本語](README.md) | [English](README.en.md)

# 信号機の作成

自作したデバイスドライバを動かす際の説明です。

# 動作環境

以下の環境にて動作確認を行っています。

- OS: Ubuntu 20.04.1 LTS

# 今回使用したもの

- raspberry pi 4 (8GB)
- 5mmLED (赤、青、黄)
- 抵抗器 (220Ω) × 6
- ユニバーサル基盤
- F-P ジャンパー線 × 6

# 配線方法

LEDのアノード側をGPIOピンに接続し、
もう一方はGNDピンに接続する。

ピンの場所がわからない場合は以下のコマンドを使用し位置の確認をする。

```sh
pinout
```

# インストール方法

```sh
cd ~
git clone https://github.com/knr2/myled.git
cd ~/myled
```

# 実行方法

実行前にmyled.cの13行目から15行目までの数値を
自分が接続したGPIOピンの番号に書き換えてください。

以下のコマンドで実行ができます。

```sh
cd ~/myled
g++ loop.cpp -o test; ./test
```

#### Videos

[![LED](http://img.youtube.com/vi/UDOO2g307oI/hqdefault.jpg)](https://youtu.be/UDOO2g307oI)