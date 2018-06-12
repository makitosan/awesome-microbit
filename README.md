# Awesome micro:bit [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

[awesome-microbit](https://github.com/carlosperate/awesome-microbit) の日本語訳

[![micro:bit logo](https://i.imgur.com/rYLbkBh.jpg)](https://www.microbit.org)

BBC micro:bit のリソースのまとめ。BBC micro:bit はプログラミング可能な小さなコンピュータで、簡単で楽しく学んだり教えられるように作られています。
この小型ボードにはブルートゥースが使えるマイクロコントローラー、USB、加速度・地磁気・明度・温度センサー、5x5 のLED、2つのボタンとGPIO（汎用入出力）があります。

Inspired by the [Awesome lists](https://github.com/sindresorhus/awesome).

この資料の修正・改善はいつでもウェルカム！（本音言うと是非貢献して欲しい）

## この資料の内容（目次）

- [プログラミング](#プログラミング)
	- [Visual](#visual)
	- [Python](#python)
	- [JavaScript / MakeCode](#javascript-and-makecode)
	- [C/C++](#cc)
	- [その他 micro:bit Languages](#その他-microbit-languages)
	- [その他 Interaction Languages](#その他-interaction-languages)
- [プログラミングツール](#プログラミングツール)
- [モバイルアプリ](#モバイルアプリ)
- [ChromeOS アプリ](#chromeos-アプリ)
- [インタフェースチップ](#いたーフェースチップ)
- [ハードウェア](#ハードウェア)
- [CAD & 3D プリンター](#cad--3d-プリンター)
- [2D デザイン](#2d-デザイン)
- [プロジェクト](#プロジェクト)
- [記事](#記事)
- [動画](#動画)
- [書籍](#書籍)
- [教材](#教材)
- [コミュニティ](#コミュニティ)
- [その他いろいろ](#その他いろいろ)

## プログラミング

### Visual

- [MakeCode](https://makecode.microbit.org) - ブラウザベースのエミュレータとブロックプログラミングで JavaScript (TypeScript) を生成できる (もともと PXT として知られていた)。
	- [MakeCode Windows 10 App](https://www.microsoft.com/store/productId/9PJC7SV48LCX) - Windows 10 で動く micro:bit MakeCode。
- [Open Roberta Lab](http://lab.open-roberta.org) - ロボットをプログラミングするためのブロックプログラミング環境で、MicroPythonを生成できるので micro:bit でも使える。
- [EduBlocks](https://microbit.edublocks.org) - Scratch から Python への経験が積める ブロックプログラミング。

以下はもうメンテナンスされてないエディタ:
- [Microsoft Blocks](https://www.microbit.co.uk/app/#create:xczaux) - Touch Develop コードを生成するブロックプログラミング。既に開発は停止し、代わりにMakeCodeの利用することを推奨。
- [Code Kingdoms](https://www.microbit.co.uk/app/#create:tomwku) - 「ドラグアンドドロップ」のプログラミングからテキストベースのプログラミング (Javascript) を経験できる。もうメンテンナンスされていない。

##### スクラッチの拡張

- [Scratch for BBC micro:bit](http://www.picaxe.com/BBC-microbit) - micro:bit を Scratch / S2Bot で Bluetooth ゲームコントローラーとして使える (特殊な BLED112 Bluetooth ドングルが必要)。
- [ScratchX micro:bit extension](https://llk.github.io/microbit-extension/) - スクラッチプログラミングで micro:bit を無線コントロールできる。
- [s2m](https://github.com/MrYsLab/s2m) - Scratch 2 のオフラインエディタと micro:bit をUSBでつなげる Python プログラム。

### Python

- [MicroPython](http://microbit-micropython.readthedocs.io) - MicroPython の micro:bit 用の移植。MicroPythonは Python 3 のマイクロコントローラーと制限された環境用の実装。

##### MicroPython エディタ

- [microbit.org Python editor](https://python.microbit.org) - micro:bit財団ウェブサイト公式の Python エディタ。
- [microbit.co.uk Python editor](http://microbit.co.uk/app/#create:xyelfe) - microbit.co.uk が提供するオリジナルの Python エディタ。古い MicroPython を含む。
- [Mu](http://codewith.mu) - MicroPython と BBC micro:bit 用の "Micro" エディタ。
- [create.withcode.uk](https://create.withcode.uk) - micro:bit MicroPython をサポートする Python のオンラインエディタとシミュレーター。 ([使い方](http://community.computingatschool.org.uk/resources/4479)).
- [Atom micro:bit MicroPython package](https://github.com/wendlers/atom-microbit-micropython) - Atom エディタ用の BBC micro:bit MicroPython サポートパッケージ。
- [Thonny micro:bit](https://bitbucket.org/KauriRaba/thonny-microbit/wiki/installation-guide) - 初心者向け Python IDE 「[Thonny](http://thonny.org)」 用のプラグイン。
- [JetBrains IDEA/PyCharm IDE plugin](https://plugins.jetbrains.com/plugin/9777-micropython-support) - IntelliJ IDEA と PyCharm 用の MicroPython プラグイン。
- [uPyCraft](https://www.gitbook.com/book/dfrobot/upycraft/details) - Windows/Mac 用の micro:bit 互換 MicroPython IDE。シンプルで使いやすくデザインされている。
- [CodeSpace](https://make.firialabs.com) - オンラインの miro:bit 用 MicroPython IDE。学習用教材もセットになっている。

##### MicroPython ライブラリ

Python 周辺知識に不足しており駄目翻訳になりそうなので後回し :wink:

- [Servo](https://github.com/microbit-playground/microbit-servo-class) - micro:bit の PWM でサーボをコントロールするシンプルなクラス。
- [PCA9685](https://github.com/gingemonster/PCA9685-Python-Microbit) - I2C 経由で PCA9685 16-Channel 12-bit PWM/Servo Driver を使うシンプルなクラス。
- [MAX7219 7-segment](https://github.com/microbit-playground/matrix7seg) - [後で] SPI 経由で ○○する MicroPython モジュール。MicroPython module for using a 7-segment display driven by a MAX7219 chip via SPI.
- [MAX7219 matrix](https://github.com/titimoby/microbit4all/blob/master/libraries/matrix7219.py) - MicroPython module for using a 8x8 Leds Matrix driven by a MAX7219 chip via SPI.
- [SSD1306](https://github.com/fizban99/microbit_ssd1306) - MicroPython library to control the OLED SSD1306 128x64 I2C with a micro:bit.
- [SSD1306 7seg](https://github.com/fizban99/microbit_ssd1306_7seg) - MicroPython library to use an SSD1306 OLED display as a 7 segment display.
- [SSD1306 SPI](https://github.com/fizban99/microbit_ssd1306spi) - MicroPython library to control the OLED SSD1306 128x64 display with a micro:bit via SPI.
- [HT16K33](https://bitbucket.org/thesheep/microbit-ht16k33) - MicroPython library for the HT16K33 LED matrix driver in multiple configurations (16x8, 8x8 or 8x8x2).
- [HC-SR04](https://github.com/fizban99/microbit_hcsr04) - Basic MicroPython library to read the distance from a HC-SR04 ultrasonic sensor using the SPI peripheral.
- [US-100](https://github.com/fizban99/microbit_us100) - Basic MicroPython library to read the distance from a US-100 ultrasonic sensor via UART.
- [KY038](https://github.com/fizban99/microbit_ky038) - MicroPython library to calibrate and use a sound sensor KY038, including clap counter functionality.
- [Nokia 5110 PCD8544 LCD](https://github.com/matneee/microbit-nokia5110-PCD8544-lcd) - Fast Micro:bit MicroPython controller for Nokia 5110 LCDs.
- [MPL115A1](https://github.com/hackscribble/microbit-MPL115A1-barometer) - MicroPython class to read the pressure and temperature readings from the NXP MPL115A1 SPI sensor.
- [24LCxxx EEPROM](https://github.com/matneee/microbit-I2C-EEPROM-24LCxxx-Read-Write) - Example Micro:bit functions to read and write to a Microchip I2C EEPROM.
- [ULN2003](https://github.com/IDWizard/uln2003) - Micropython code to drive stepper motors via ULN2003 darlington transistors.
- [Bosch BME280](https://github.com/jemerlia/microbit-BoschBME280-P-T-and-H-Sensor) - Reading from Bosch BME280 Pressure, Temperature and Humidity Sensor via I2C.
- [Pixy](https://github.com/liamkinne/microbit-pixy) - Interface module for using the Pixy cam with the BBC micro:bit.
- [MB1013](https://github.com/liamkinne/microbit-mb1013) - Module for the MB1013 ultrasonic sensor controlled via UART.
- [MY9221](https://github.com/mcauser/microbit-my9221) - Library for 10 segment LED bar graph modules using the MY9221 LED driver.
- [AM2320](https://github.com/mcauser/microbit-am2320) - Library for interfacing with an Aosong AM2320 temperature and humidity sensor over I2C.
- [DHT12](https://github.com/mcauser/microbit-dht12) - Library for interfacing with an Aosong DHT12 temperature and humidity sensor over I2C.
- [TM1637](https://github.com/mcauser/microbit-tm1637) - Library for quad 7-segment LED display modules using the TM1637 LED driver.
- [micro:bit MIDI](https://github.com/liamkinne/microbit-midi) - Module to enable talking to MIDI devices on the BBC micro:bit.

##### Python ライブラリ

- [MicroPeri](https://github.com/c0d3st0rm/microperi) - micro:bit を外部ペリフェラルまたはセンサとして接続し、micro:bit MycroPython と同じAPIで動かすための Python ライブラリ。
- [microbit_stub](https://github.com/casnortheast/microbit_stub) - micro:bit の MicroPython API をエミュレートするライブラリ。
- [bluezero](https://github.com/ukBaz/python-bluezero) - micro:bit の事例がある Bluetooth デバイスと接続するための Python ライブラリ。
- [bitio](https://github.com/whaleygeek/bitio) - micro:bit I/O 用の Python ライブラリ。PC/Mac/Linux/Rasberry Pi で Python コードを実行でき、 micro:bit と直接やり取りさせることができる。

##### Python プログラミングツール

- [uFlash](https://github.com/ntoll/uflash/) - Python のプログラムで micro:bit を書き換えるツール。
- [MicroFs](https://github.com/ntoll/microfs) - micro:bit のファイルシステムとやり取りするコマンドラインツールと Python モジュール。
- [Jupyter kernel for the micro:bit](https://github.com/takluyver/ubit_kernel) - Jupyter が直接 MicroPython のコードを micro:bit 上で動かせるようにするパッケージ。

### JavaScript and MakeCode

- [MakeCode](https://makecode.microbit.org) - micro:bit 用のブラウザベースのエミューレーター、ブロックプログラミング、JavaScript(TypeScript)エディター
	- [MakeCode Windows 10 App](https://www.microsoft.com/store/productId/9PJC7SV48LCX) - Windows 10 で動く micro:bit MakeCode
- [Espruino JavaScript](http://www.espruino.com/MicroBit) - マイクロコントローラー用の JavaScript インタープリター。 テキスト及びブロックでコードが書ける WebIDE もある。

##### MakeCode 用パッケージ

MakeCode 上でパッケージインストールして使うもの。ベータ版のものが多いので利用は自己責任で。

- [Neopixel](https://github.com/Microsoft/pxt-neopixel) - Neo-Pixel (個別のアドレス可能な RGB LED) 用パッケージ。
- [Filesystem](https://github.com/Microsoft/pxt-filesystem) - ベータ版のファイルシステムパッケージ。
- [MAX6675](https://github.com/Microsoft/pxt-max6675) - MAX6675 (デジタル温度計) 用パッケージ。
- [Bluetooth MAX6675](https://github.com/Microsoft/pxt-bluetooth-max6675) - MAX6675(デジタル温度計)用の Bluetooth サービス。
- [Sonar](https://github.com/Microsoft/pxt-sonar) - HC-SR04等の超音波距離センサモジュール用のパッケージ。
- [Bluetooth Temperature Sensor](https://github.com/Microsoft/pxt-bluetooth-temperature-sensor) - 温度読み出し用の Bluetooth サービス。
- [MIDI](https://github.com/Microsoft/pxt-midi) - MakeCode 用の MIDI インタフェース。
- [Bluetooth MIDI](https://github.com/Microsoft/pxt-bluetooth-midi) - MakeCode 用の Bluetooth Midi インタフェースパッケージ。
- [BlueDot](https://github.com/Microsoft/pxt-bluedot) - BlueDot アプリをサポートするパッケージ。
- [GY521](https://github.com/PaulDFoster/pxt-microbit-GY521) - MPU-6050 (GY-521 三軸ジャイロセンサ) 用パッケージ。
- [UCL Junkrobot](https://github.com/chevyng/pxt-ucl-junkrobot) - 28BYJ-48 ステッパーモーターと HC-SR04 超音波センサーを使用して動かすジャンクロボット用パッケージ。
- [BitBot](https://github.com/srs/pxt-bitbot) - BitBot 用パッケージ。
- [gamer:bit](https://github.com/sparkfun/pxt-gamer-bit) - SparkFun gamer:bit (ゲームコントローラ風のモジュール) 用パッケージ。
- [moto:bit](https://github.com/sparkfun/pxt-moto-bit) - SparkFun moto:bit (車両等を作るためのボード) 用パッケージ。
- [weather:bit](https://github.com/sparkfun/pxt-weather-bit) - SparkFun weather:bit （天気関係の気圧、温度、湿度等のセンサが付いたボード）用パッケージ
- [SSD1306](https://github.com/Tinkertanker/pxt-ssd1306-microbit) - SSD1306 OLED （有機ELディスプレイ）  コントローラー用のパッケージ
- [mi:node](https://github.com/minodekit/pxt-minode) - mi:node kit (element14が提供しているIoTスターターキット) 用のパッケージ。
- [Kitronik Servo Lite](https://github.com/KitronikLtd/pxt-kitronik-servo-lite) - Kitronik Servo:Lite (サーボコントロール用ボード) 用パッケージ。
- [Kitronik I2C 16 Servo](https://github.com/KitronikLtd/pxt-kitronik-I2C-16-servo) - Kitronik I2C 16 (最大16個のサーボをコントロールするボード) 用パッケージ。
- [Kitronik motor driver](https://github.com/KitronikLtd/pxt-kitronik-motor-driver) - Kitronik Driver Board (micro:bit 用モーター基板) 用パッケージ。
- [Lego Power Functions](https://github.com/philipphenkel/pxt-powerfunctions) - LEGO® Power Functions モーターを micro:bit と 赤外線 LED を使ってコントロールするパッケージ。
- [KY040](https://github.com/Tinkertanker/pxt-ky040-microbit) - LY-040 ロータリーエンコーダー用パッケージ。
- [Invent robot](https://github.com/techcampuk/pxt-invent) - Invent ロボット作成キット用のパッケージ。
- [Robotbit](https://github.com/KittenBot/pxt-robotbit) - KttenBot Robotbit 用パッケージ。
- [ubirch NB-IoT](https://github.com/ubirch/pxt-ubirch) - ubirch バックエンドへの署名済みデータ送信用パッケージ。
- [CCS811](https://github.com/ADataDate/pxt-airQuality) - CCS811 空気品質センサモジュール用パッケージ。
- [DS1307](https://github.com/Tinkertanker/pxt-ds1307-microbit) - DS1307 RTC (リアルタイムクロックモジュール) 用パッケージ。
- [HT16K33](https://github.com/Tinkertanker/pxt-ht16k33-alnum4) - HT16K33 I2C Alphanumeric Display (アルファベット用ディスプレイ) 用パッケージ。
- [HoneyBit](https://github.com/HoneycombKits/pxt-HoneyBit) - Honeycomb キット用パッケージ。
- [katakana](https://github.com/mbitfun/pxt-katakana) - 半角カタカナを micro:bit に表示するパッケージ。
- [Bluetooth beacons](https://github.com/kshoji/pxt-bluetooth-beacons) - Bluetooth ビーコン用パッケージ。 iBeacon や AltBeacon アドバタイザーみたいなことができる。
- [micro turtle](https://github.com/Microsoft/pxt-microturtle) - micro:bit のスクリーン上で1つのピクセルを動かす（亀に見立てて）パッケージ。LOGO言語っぽく書ける。
- [Grove](https://github.com/seeed-studio/pxt-grove) - Seeed Studio Grove モジュール用のパッケージ。
- [LumexOLED](https://github.com/lioujj/pxt-oled) - Lumex LED用パッケージ。

##### Node.js ライブラリ

- [node-bbc-microbit](https://github.com/sandeepmistry/node-bbc-microbit) - BLE を使って Node.js から micro:bit をコントロール。
- [node-bbc-microbit-io](https://github.com/sandeepmistry/node-bbc-microbit-io) - Johnny-Five (JavaScript Robotics と IoT 用プログラミングフレームワーク) 用 micro:bit IO プラグイン。

##### JavaScript ブラウザライブラリ

- [microBit.js](https://github.com/antefact/microBit.js) - Web Bluetooth API を使用して BBC micro:bit とやり取りする JavaScript ライブラリ。

##### JavaScript プログラミングツール

- [PXT Command Line Tool](https://makecode.com/cli) - コマンドラインツールで MakeCode JavaScript のプログラムを micro:bit にインストールできる。また、ローカルバージョンの MakeCode エディタを実行可能。

### C/C++

- [C/C++ runtime](https://lancaster-university.github.io/microbit-docs/) - C/C++ で micro:bit プログラムを始めるためのガイドで、micro:bit ランタイムを構成するAPI、ドライバーと型の全てのドキュメントがある。Bluetooth のドキュメントに工場出荷時の micro:bit のオリジナル hex ファイルへのリンクがある。
- [Arduino nRF5](https://github.com/sandeepmistry/arduino-nRF5/) - micro:bit を含む Nordic Semiconductor nRF5 ベースの基盤用の Arduino コア。

##### C/C++ エディタ

- [Micro:Pi](https://github.com/Bottersnike/Micro-Pi) - シリアルモニターとデプロイ機能付きの micro:bit 用の C/C++ 用エディタ。Python で書かれ、全ての依存関係を含んだインストーラー付き（インストーラーはATM Linux のみで動作し、その他のOSでは手動でインストールする必要がある）。

##### C/C++ ライブラリ

- [OneWire](https://github.com/adamboardman/microbit-onewire) - BBC micro:bit OneWire ライブラリ, Erik Olieman の mbed DS1820 lib を基にしたもの。
- [neopixel](https://github.com/elmorg/uBit_neopixel) - neopixels を BBC micro:bit で使うためのライブラリ。
- [micro:bit Screen](https://github.com/ht-deko/microbit_Screen) - micro:bit 用 Arduino LED スクリーンライブラリ。
- [Adafruit Arduino micro:bit library](https://github.com/adafruit/Adafruit_Microbit) - Arduino IDE で micro:bit を使うためのラッパーコードとサンプル。
- [RTCC MCP7941X](https://os.mbed.com/users/euxton/code/microbit-RTCC-MCP7941X/) - BBC micro:bit から MCP79410 RTCC (Real Time Clock Calendar) モジュールとやり取りするプログラム。
- [AS-289R2](https://os.mbed.com/users/MACRUM/code/microbit_AS-289R2/) - micro:bit 用 AS-289R2 サーマルプリンター Mbed ライブラリ。

### その他 micro:bit Languages

その他の micro:bit をプログラム可能なプログラミング言語

- [Touch Develop](https://www.microbit.co.uk/create-code#touchdevelopEditor) - インタラクティブなビジュアルコンポーネントを使ってテキストベースのプログラミング柔軟にできる。
- [Rust](https://github.com/SimonSapin/rust-on-bbc-microbit) - Rust で書かれたコードを micro:bit 用にコンパイルしたときの話を書いた記事。
- [Forth](https://wiki.forth-ev.de/doku.php/en:projects:microbit:start) - BBC micro:bit 用のスタックベースのプログラミング言語。
- [Pascal](http://wiki.freepascal.org/micro:bit) - micro:bit を含む ARM プロセッサーベース向けのパスカルコンパイラ。
- [Ada](https://github.com/AdaCore/Ada_Drivers_Library/tree/master/examples/MicroBit) - micro:bit 用の Ada 開発環境をセットアップする手順。
- [Sniff](http://www.sniff.org.uk/p/bbc-microbit.html) - Sniff は Scratch のようなプログラム言語で、Scratch から従来のプログラミング言語にスムーズに移行できるようにデザインされている。
- [Lisp](http://www.ulisp.com/show?2672) - BBC micro:bit 用の Lisp インタプリター。

### その他 Interaction Languages

これらのプログラミング言語は直接 micro:bit にプログラムしないが、micro:bit をやり取りするプログラムを書くときに使えるもの。

- [Kodu Controller](http://www.kodugamelab.com/bbc-microbit/) - Kodu Game Lab から micro:bit とやり取りできる。
- [Simulink Coder Support Package](http://www.mathworks.com/help/supportpkg/microbit/) - Simulink のモデルを作成でき、自動的に micro:bit にインストールできるパッケージ。.
- [micro:bit for Dyalog APL on the Pi](https://github.com/APLPi/microbit) - Raspberry Pi 上の Dynalog APL から micro:bit を（MicroPython のシリアルコネクション経由で）使うツール。
- [Gobot](https://gobot.io/documentation/platforms/microbit/) - 現実のデバイスをプログラムする Go 言語のフレームワーク。micro:bit と Bluetooth LE 経由でやり取りできる。
- [Microbit-Unity](https://github.com/bLiGM/Microbit-Unity) - Unity Controller として BBC micro:bit を使うための Unity スクリプト。
- [Haxe node BBC micro:bit](https://github.com/MatthijsKamstra/hx-node-bbc-microbit) - Node.js から BLE と Haxe 言語を使って BBC micro:bit をコントロールする。
- [App Inventor + IoT](http://iot.appinventor.mit.edu/#/microbit/microbitintro) - App Inventor を使って Bluetooth 経由で micro:bit をコントロールする。App Inventor は Android アプリ用のビジュアルプログラミング言語。
- [BlockyTalkyBLE](http://www.playfulcomputation.group/blockytalkyble.html) - Bluetooth 経由で BBC micro:bit と AppInventor のモバイルアプリを簡単に接続できるようにする MakeCode と App Inventor の拡張。
- [DroidScript micro:bit Plugin](https://play.google.com/store/apps/details?id=org.droidscript.microbit) - DroidScript アプリ（JavaScriptで書かれたAndroidアプリ）から BBC micro:bit を無線でコントロールできるようにするプラグイン。
- [CBMicroBit](https://github.com/Louismac/CBMicroBit) 「C++/Objective C」 用の C++ で書かれた コア Bluetooth ラッパーで、OSX と micro:bit をBLEで接続し、OSC経由で出力ができる（単独での使用したり、C++ や Objective C のライブラリとして使える）。
- [Swift](https://github.com/phwallen/microbit-swift) - Swift で書かれた micro:bit を使う API。BLE経由で Apple デバイスと micro:bit のやり取りができるようになる。

## プログラミングツール

- [Vagrant Development Environment for C/C++, MicroPython and Makecode](https://github.com/carlosperate/microbit-dev-env) - micro:bit 開発に必要なツール群、C/C++ プログラム、MicroPython の開発/コンパイル、MakeCode用パッケージの作成っといったものが入ったVagrant VM。
- [micro:bit uploader](https://www.touchdevelop.com/microbituploader) - ダウンロードフォルダを監視して自動的に micro:bit にインストールするWindowsアプリケーション。

## モバイルアプリ

- [Official Android App](https://play.google.com/store/apps/details?id=com.samsung.microbit) ([Source Code](https://github.com/Samsung/microbit)) - Bluetooth 経由で micro:bit のプログラムを書き換えられる。
- [Official iOS App](https://itunes.apple.com/gb/app/micro-bit/id1092687276) - Bluetooth 経由で micro:bit のプログラムを書き換えられる。
- [micro:bit Blue](https://play.google.com/store/apps/details?id=com.bluetooth.mwoolley.microbitbledemo) ([Source Code](https://github.com/microbit-foundation/microbit-blue)) - Bluetooth を使用して micro:bit とやり取りするいくつかのデモを含んだ Android アプリ。
- [Bitty Software Apps](http://www.bittysoftware.com/apps.html) - いろんな Android 及び iOS アプリの一覧で、中にはデータ収集、音を鳴らす等があり、興味のあるものが見つけられるかも。
- [Insight Mr Bit](http://www.insightresources.co.uk/microbit/page63.html) ([iOS](https://itunes.apple.com/gb/app/insight-mr-bit/id1175915875)) - シンプルなプログラムを簡単な英語で作成し便利なことが色々するように BBC micro:bit をコントロールする。
- [Micro:bit Xamarin](https://play.google.com/store/apps/details?id=com.sumitgouthaman.microbitble) ([Source code](https://github.com/sumitgouthaman/microbit-ble-mobile)) - BBC micro:bit と Bluetooth LE 経由でやり取りするデモ用 Android アプリ。オープンソースのアプリなので、Xamarin で micro:bit を扱う良い事例。
- [bitty blue](http://www.bittysoftware.com/apps/bitty_blue.html) - BBC micro:bit と Bluetooth で色々楽しめる iOS と Android アプリ。
- [micro:bit logger](https://play.google.com/store/apps/details?id=nl.defbu.mblogger) - BLE 経由でデータを収集しファイルに出力できる Android アプリ。
- [Kitronik Move](https://play.google.com/store/apps/details?id=com.kitronik.kitronikmove) - Bluetooth LE 経由で micro:bit をコントロールする十字キー Android アプリ。
- [nRF Connect](https://play.google.com/store/apps/details?id=no.nordicsemi.android.mcp) - BLE デバイスのスキャン、アドバタイズ、捜査ができる Android 用ツールアプリ。micro:bit も対応し、サービス情報やマクロ等が使える。
- [Tickle](https://tickleapp.com) - micro:bit を含む多種のデバイスをプログラム可能な iOS アプリで、お互いを接続し互いにやり取りさせられる。
- [Serial Bluetooth Terminal](https://play.google.com/store/apps/details?id=de.kai_morich.serial_bluetooth_terminal) - micro:bit の Bluetooth UART データを送受信できる Android アプリ。

## ChromeOS アプリ

- [Quiz:bit](https://chrome.google.com/webstore/detail/quizbit/hfnanbphehfnlcpkelfnkmfdljphlmna) ([Source Code](https://github.com/lancaster-university/quiz-bit)) - BBC micro:bit programs and a matching application for providing a quiz-voter-style service using micro:bits as the controls.
- [bitty blue](http://www.bittysoftware.com/apps/bitty_blue.html) - Play with 3D "PolySquiggles", use as a compass, have fun with the buttons, send images or text to the LED display, connect and control electronic circuits, and all via Bluetooth.
- [bitty data logger](http://www.bittysoftware.com/apps/bitty_data_logger.html) - Capture and chart accelerometer, magnetometer and temperature data from your micro:bit's internal sensors over Bluetooth.
- [microbit-chrome](https://github.com/Microsoft/microbit-chrome) - Prototype chrome addon that exposes the micro:bit's serial output to webpages like the MakeCode editor.


## インターフェースチップ

USB インタフェースチップはバッテリーコネクタのそばに配置されたマイクロコントローラーで、USB のストレージ・デバイスとして動作し、オペレーティング・システムのファイルエクスプローラーを使った micro:bit のファームウェアの更新をができるようになっている。

- [microbit.org Developer Community Info](http://tech.microbit.org/software/daplink-interface/) - この micro:bit の開発者コミュニティページにはインタフェースチップの DAPlink と USB インタフェースの情報がある。
- [DAPLink on micro:bit](https://www.mbed.com/en/development/hardware/prototyping-production/daplink/daplink-on-kl26z/) - DAPLink はインタフェースチップ上で動く標準のソフトウェアで、このページには更新方法や最新のファームウェアの情報がある。
- [DAPLink source code](https://github.com/mbedmicro/DAPLink) - mbed DAPLink のソースコード。micro:bit用のビルド情報もある。
- [J-Link OB Firmware](https://www.segger.com/bbc-micro-bit.html) - DAPLink と同等の書き換え機能があり、J-Link デバッグを含んだ拡張ができる。
- [pyOCD](https://github.com/mbedmicro/pyOCD) - micro:bit に備わっている ARM Cortex-M マイクロコントローラーのプラグラム及びデバッグ用の Python ライブラリ。インターフェースチップから提供された CMSIS-DAP を使っている。:cry: 専門知識が不足して何言ってるかわからん
- [DAP.js](https://github.com/ARMmbed/dapjs) - USB/HID 経由の JavaScript (Node.js and WebUSB)インタフェースから DAP-CMSIS とやり取りする。つまり、pyOCD の機能のサブセット。

## ハードウェア

- [Hardware Design](https://github.com/bbcmicrobit/hardware) - BBC micro:bit の回路図と部品表。
- [micro:bit Reference Design](https://github.com/microbit-foundation/microbit-reference-design) - micro:bit と100%のバイナリ互換のある基盤のデザインファイル。独自の micro:bit を設計するとき用。
- [micro:bit Badge](https://github.com/make-zurich/micro-bit-badge) - バッテリーホルダ、ブザー、コネクタの拡張、ピンの接続部分を備えた オープンソース PCB （プリント基板）。
- [Eagle micro:bit Edge Part](https://github.com/proto-pic/micro-bit-eagle-libraries) - micro:bit のエッジコネクタ用の Eagle ライブラリ。
- [Kicad micro:bit Connector](https://github.com/anthonykirby/kicad_microbit_connector) - micro:bit のエッジコネクタソケット用の KiCad コンポネントライブラリとフットプリント（PCB部品形状）ライブラリ。
- [SparkFun Breakout Board](https://github.com/sparkfun/Micro_Bit_Breakout) - SparkFun micro:bit ブレークアウト基板用のオープンソースファイル。
- [SparkFun moto:bit](https://github.com/sparkfun/Micro_Bit_Moto_Bit) - SparkFun moto:bit 用のオープンソースファイル。moto:bitはロボットプラットフォームの基板。
- [SparkFun weather:bit](https://github.com/sparkfun/Micro_Bit_Weather_Bit) - SparkFun weather:bit 用のオープンソースファイル。これは気象台用の基板。
- [SparkFun gamer:bit](https://github.com/sparkfun/Micro_Bit_Gamer_Bit) - SparkFun gamer:bit 用のオープンソースファイル。ゲームシステム用の基板。

## CAD & 3D プリンター

- [Kitronik CAD Resources](https://www.kitronik.co.uk/blog/bbc-microbit-cad-resources/) - Kitronik で生成された BBC micro:bit CAD モデル。
- [Proto-PIC CAD Resources](https://www.proto-pic.co.uk/micro-bit-resources.html) - Proto-PIC の micro:bit 関連製品の CAD リソース。
- [Microbot Case](http://www.thingiverse.com/thing:1434797) - micro:bit 用のロボットの形をした3Dプリンタ製ケース。
- [micro:bit Stand](http://www.thingiverse.com/thing:2144500) - 3Dプリンタ製の micro:bit 用スタンド。
- [micro:bit Rover](https://www.myminifactory.com/object/microbit-rover-27013) - micro:bit ロボットローバーを作るための3Dプリンタ製のパーツ。
- [micro:Racing](https://www.myminifactory.com/object/micro-racing-18280) - micro:bit 用の3Dプリンタ製の3Dハンドル型のケース。
- [Binary Watch](https://www.myminifactory.com/object/binary-watch-15257) - micro:bit 用の3Dプリンタ製の時計とストラップ。
- [micro:bit Compass](https://www.myminifactory.com/object/micro-bit-compass-18994) -micro:bit 用の3Dプリンタ製のコンパスケース。
- [A4 folder holder](https://www.myminifactory.com/object/micro-bit-a4-folder-holder-22039) - A4サイズのスクールフォルダ（リングファイル）に収めるための micro:bit 用の3Dプリンタ製ホルダー。
- [mibot drawing robot](https://www.myminifactory.com/object/mibot-drawing-robot-36030) - BBC micro:bit とモータードライブ基板でできたお絵かきロボット用の3Dプリンタ製シャーシ（胴体）。
- [Robottillo:bit](https://www.myminifactory.com/object/robottillo-bit-46478) - 小さなロボットみたいな見た目の3Dプリンタ製のケース。2つのバージョンが有り、背面を保護するものとピン用の穴が空いたもの。
- [Battery pack holder](https://www.thingiverse.com/thing:2666671) - BBC micro:bit 用のシンプルな3Dプリンタ製電池パックホルダ。
- [micro:bit holder](https://www.thingiverse.com/thing:2750805) - 20個のmicro:bitを縦置きできるスタンドで、教室で使うと便利なもの。

## 2D デザイン

- [micro:bit Fritzing Part](https://github.com/topshed/FritzingParts) - micro:bit 用のモデルもある Fritzing パーツの Richard Hayler さんのコレクション。
- [micro:bit-o-matic](https://pycomic.github.io/microbit.html) - ウェブサイトで使える簡単に mciro:bit のLEDメッセージ付きのイラスト（画像）を生成できる。
- [micro:bit SVG](https://github.com/microbit-foundation/microbit-svg) - 精細なSVG製の BBC micro:bit 画像。
- [MonkMakes micro:bit Diagramming Kit](https://github.com/simonmonk/mm_mb_diagramming_kit) - BBC micro:bit のワニクリップを使ったダイアグラム図を作成するときに使えるSVGファイルテンプレート

## プロジェクト

これらのプロジェクトには再現可能な手順と材料が含まれています。

- [JUST DO IoT](https://hackaday.io/project/12164-just-do-iot) - LoRaWAN ネットワークに micro:bit を接続。オープンソースの micro:bit に接続するハードウェアも含む。
- [Micro:Bob](https://hackaday.io/project/8643-microbob) - micro:bit でコントロールできる簡単な二足歩行ロボット。
- Coffee Timer ([1](https://www.norwegiancreations.com/2016/09/coffee-timer-part-1-the-first-prototype-based-on-the-bbc-microbit/), [2](https://www.norwegiancreations.com/2016/10/coffee-timer-part-2-low-power-wireless-on-the-bbc-microbit/), [3](https://www.norwegiancreations.com/2016/11/coffee-timer-part-3-enclosures/)) - コーヒーメーカーを micro:bit のインジケーターで拡張することに関する3つの記事。省電力通信の選択肢と特別な筐体の作成方法等。
- [Thermal Printer](http://www.suppertime.co.uk/blogmywiki/2016/12/microbit-thermal/) - Spakfun 感熱チルロールプリンターに接続して使用する。
- [Telescopic Light Sword](https://www.myminifactory.com/object/telescopic-lightsword-with-micro-bit-14598) - micro:bit と電気と3Dプリンタパーツを使ってオリジナルの光の剣を作るプロジェクト。
- [Micro Simon](http://mrtomsworld.blogspot.co.uk/2017/01/micro-simon.html) - micro:bit をあのサイモンゲームに接続してプログラムする。
- [Alexa Weather On micro:bit](https://www.hackster.io/chen-tiebiao/weather-on-micro-bit-c79c19) - 天気をきかれたときに回答を micro:bit に表示する Amazon Alexa のような機能。
- [BBC Microbit Balloon Tracker](http://www.daveakerman.com/?p=2019) - micro:bit を GPS と LoRa トランシーバーを接続して現在地を追跡送信するバルーントラッカー。
- [SonicPixels](https://github.com/jrmedd/SonicPixels) - BBC micro:bit と Max フレームワークを使い複数のスピーカーをコントロール。
- [Little Bug Bit](http://goo.gl/eEFhcy) - ローコスト micro:bit バギー（リンク先は Google アカウント必要）。
- [HandShake](https://sites.google.com/site/hardwaremonkey/home/handshake) - 体が不自由な人向けのジェスチャー認識プロジェクト。
- [Mega:Bit](http://www.makerspace-uk.co.uk/megabit/) - micro:bit の 5x5 LED とボタンをを巨大化して本物の micro:bit を接続する。
- [Scrolling display](https://meanderingpi.wordpress.com/2017/09/16/bbc-microbit-scrolling-display/) - 無線で複数の micro:bit を接続して作るスクリーンディスプレイ。
- [Ironman Arc Reactor](https://www.kitronik.co.uk/blog/halo-ween-ironman-arc-reactor) - 3D プリンターで部品を作り組み立てられる micro:bit で接続されたアイアンマンのアークリアクターで 。MK I と Mk II を選択可能。
- [microbit-beacon-finder](https://github.com/kshoji/microbit-beacon-finder) - BLE ビーコンを探し、そのIDを micro:bit のLEDに表示。
- [Build A Klawsome micro:bit Controlled Tank](https://www.kitronik.co.uk/blog/klawsome-microbit-controlled-tank/) - パースペックス材の micr:bit 戦車の設計方法。 [micro:bit Hovercraft](http://www.instructables.com/id/Make-a-Cool-Microbit-Hovercraft-Together/) - 水陸両用ホバークラフト。車体を浮上させる下向きに空気を送る二つのモーターと、方向をコントロールする2つのモーターを使う。
- [ZIP Halo Compass](https://www.kitronik.co.uk/blog/bbc-microbit-zip-halo-compass) - クリスマステーマの micro:bit ZIP Halo コンパス。ケースは3Dプリンタ製でレーザーカットされたもの。
- [Micro:Boy](https://hackaday.io/project/27757-microboy) - micro:bit でアーケードゲームを作って遊ぶハードウェアプロジェクト。
- [Alexa, Ask micro:bit to Turn LED Light](https://medium.com/@ferrygunawan/alexa-ask-microbit-to-turn-led-light-61ed668a0321) - Alexa と RGB LED と micro:bit を接続してコントロールするプロジェクトの解説。
- [OpenGestureControl](https://opengesturecontrol.github.io) - 義手の人がジェスチャーでデスクトップコンピュータをコントロールするための BBC micro:bit とやり取りする Linux アプリケーション。
- [micro:bit spectrum](https://github.com/linker3000/micro-bit_spectrum) - BBC micro:bit にオーディオスペクトラムを表示する回路とコード。
- [micro:bit TVPong](https://github.com/linker3000/Microbit-TVPong) - TVで古くからあるPongゲームを遊ぶ。BBC micro:bit をコントローラーに、BLEを使う。

### Project コレクション

- [microbit.co.uk Site Index](https://www.microbit.co.uk/index) - microbit.co.uk にはプロジェクトやチュートリアルがそろった大規模なリストがある。
- [hackster micro:bit community](https://microbit.hackster.io) - ユーザーが投稿した micro:bit 用プロジェクトがある hackster のコミュニティ。
- [MakeCode Projects](https://makecode.microbit.org/projects/) - MakeCode エディタでできる micro:bit プロジェクトの一覧。
- [Inventorspace micro:bit category](https://invent.sparkfun.com/cwists/category#products=%5B8%5D) - SparkFunが提供する、教室や学校、学区で実践できる楽しいプロジェクトのコミュニティ。
- [Tinkercademy Projects](https://tinkercademy.com/microbit/) - micro:bit と Tinkercademy Tinker Kit を使ったプロジェクトのコレクション。
- [Raspberry Pi micro:bit Projects](https://projects.raspberrypi.org/en/projects?technologies%5B%5D=microbit) - Raspberry Pi 財団が提供する Raspberry Pi と micro:bit を使ったプロジェクトのコレクション。
- [Hackaday.io micro:bit Projects](https://hackaday.io/projects?tag=micro%3Abit) - Hackaday.io 内の 「micro:bit」 タグが付いたプロジェクト。 Hackaday.io はコラボレーションできるハードウェア開発コミュニティ。


## 記事

micro:bit 開発関連の便利な記事

- [Offline C/C++ Development With The Micro:bit](http://www.i-programmer.info/programming/hardware/9654-offline-cc-development-with-the-microbit-.html)
- [Sending 'commands' from a micro:bit over Bluetooth](http://bluetooth-mdw.blogspot.co.uk/2016/07/sending-commands-from-microbit-over.html)
- [Modelling micro:bit data with the Bitty Data Logger App](https://www.stem.org.uk/elibrary/community-resource/289686/modelling-microbit-data-bitty-data-logger-app)
- [Getting Started with the micro:bit Bluetooth IO Pin Service](https://ukbaz.github.io/howto/ubit_ble_profile.html)
- [Using MQTT-SN over BLE with the BBC micro:bit](https://blog.benjamin-cabe.com/2017/01/16/using-mqtt-sn-over-ble-with-the-bbc-microbit)
- [The First Video Game on the BBC Micro:bit [probably]](https://hackernoon.com/the-first-video-game-on-the-bbc-micro-bit-probably-4175fab44da8) - micro:bit 用ゲーム作成。パフォーマンス向上に必要な MicroPython の変更箇所やリソースの一般的なプロファイルの話。
- [Custom BLE services with micro:bit](https://www.hackster.io/pelikhan/custom-ble-services-with-micro-bit-6c9879) - 初心者でも使える PXT/MakeCode ブロックとして使える Bluetooth LE サービスの作り方。
- [Excel and Micro:Bit - Hacking for fun and creativity!](https://techcommunity.microsoft.com/t5/Excel-Blog/Excel-and-Micro-Bit-Hacking-for-fun-and-creativity/ba-p/63603) - マイクロコントローラーを使った基本的なセンサーデータの収集の実験と、データのExcelを使ったビジュアル化。
- [Writing the second video game for the Micro:bit in Rust](https://hackernoon.com/writing-the-second-video-game-for-the-micro-bit-in-rust-3cd8b5ab22d3) - micro:bit ゲームの変更と Rust 言語への移植。
- [Adding a new module to MicroPython](http://cigdemsengul.blogspot.co.uk/2017/04/offline-development-in-microbit-adding.html) - midro:bit 用の新しいモジュールを MicroPython に追加する実験の記事。
- [Become a Time Lord with the BBC micro:bit](https://blog.groklearning.com/become-a-time-lord-with-the-bbc-micro-bit-c4b8b4e2d747) - MicroPython で複数のことを実行するための異なるタイミングメカニズムの使い方について。
- [Debugging the micro:bit with pyOCD and GDB](https://docs.mbed.com/docs/mbed-os-handbook/en/5.4/debugging/debugging_microbit/) - PyOCDとGDBを使った micro:bit のデバッグ方法。
- [Exploring the BBC micro:bit Software Stack](http://mattwarren.org/2017/11/28/Exploring-the-BBC-microbit-Software-Stack/) - 何があって、何をして、全部をどう組み合わせるのかについて。
- [Building the 1,000 BBC micro:bit Display](https://www.kitronik.co.uk/blog/building-the-bbc-microbit-matrix-display/) - 1000個の BBC micro:bit から画像を表示するスクリーンが作れるのか？
- [micro:bit Radio Packets](https://ukbaz.github.io/howto/ubit_radio.html) - MakeCode の無線パケットの仕様の説明（micro:bit ランタイム仕様上に構築されているもの）と MakeCode と MicroPython プログラムを無線経由でやり取りする方法について。
- [Synchronized Music on micro:bits](https://blog.flowblok.id.au/2018-02/synchronized-music-on-microbits.html) - micro:bit のメッシュネットワークを構築し、広いエリアで音楽を同調して流す仕組みを構築。
- [Using the Built-in Sensors](https://learn.adafruit.com/micro-bit-lesson-1-using-the-built-in-sensors) - micro:bit に付属している加速度センサーと地磁気センサーの使い方を学ぶ。

### 記事 コレクション

- [MultiWingSpan](http://www.multiwingspan.co.uk/micro.php) - 電子部品の使い方に関する例と説明、指示書の大規模なコレクション。
- [ElecFreaks micro:bit category](https://www.elecfreaks.com/blog/micro-bit/) - 個々のセンサーや部品の使い方のコンセプトを解説する実験を集めた ElecFreaks のコレクション。
- [SparkFun micro:bit tutorials](https://learn.sparkfun.com/tutorials/tags/microbit) - SparkFun が提供する彼らのキットの広範囲の実験ガイドを含んだ解説のコレクション。
- [BitIO blogs](http://warksjammy.blogspot.co.uk/2017/07/bitio-blogs-in-one-place.html) - micro:bit をコントロールする BitIO Python モジュールの使い方に関するブログ記事のコレクション。
- [micro:bit learning](http://www.microbitlearning.com/tag/microbit) - micro:bit や Arduino 用の様々な種類のセンサーの使い方の記事。
- [Adafruit Learn micro:bit section](https://learn.adafruit.com/category/micro-bit) - BBC micro:bit に関する Adafruit Learning System の記事。
- [BBC micro:bit - Kitronik University](https://www.kitronik.co.uk/blog/bbc-microbit-kitronik-university/) - Kitronik 提供の様々な micro:bit のコレクション。

## 動画

- [MicroMonsters](https://www.youtube.com/channel/UCK2DviDexh_Er2QYZerZyZQ) - 家族と一緒にコーディングを学べる YouTube チャネル。
- [micro:bit and Bluetooth](https://www.youtube.com/playlist?list=PLYOCnwH2UtBzhJ2nvn_DM3itz6GNVwrDu) - Martin Woolley のブルートゥース動画の YouTube プレイリスト。
- [Video Series from The Maker Movies](https://www.youtube.com/playlist?list=PLD0HD_3AJljXDWoasq2x5gHmkKeV7cc-P) - micro:bit 初心者用の短い解説ビデオの一覧。
- [SparkFun video resources](http://sparkfuneducation.com/video-resources/microbit.html) - micro:bit 用の動画教材の現在進行系で追加されている一覧。
- [SamCodes YouTube Playlist](https://www.youtube.com/playlist?list=PLumNlyd5JxxegaAVScP7Qm1AXPtJdGBCq) - 異なる micro:bit 用の電子部品と機能の使い方の動画解説。
- [Fun with Zephyr Project and BBC micro:bit](https://www.youtube.com/watch?v=ZZRbIpVJGns) - Zephyr を使って micro:bit とブルートゥースチップを拡張する方法の解説動画。

## 書籍

- [micro:bit IoT In C](http://www.iot-programmer.com/index.php/books/micro-bit-iot-in-c)
- [Programming with MicroPython](http://shop.oreilly.com/product/0636920056515.do)
- [Getting Started with the micro:bit](http://shop.oreilly.com/product/0636920115267.do)
- [The Official BBC micro:bit User Guide](https://www.wiley.com/en-gb/The+Official+BBC+micro:bit+User+Guide+-p-9781119386735)
- [Programming the BBC micro:bit](http://simonmonk.org/prog-mb/)
- [Networking with the micro:bit (ebook)](https://microbit.nominetresearch.uk/networking-book/)
- [micro:bit in Wonderland](http://www.techagekids.com/2017/11/our-beginner-bbc-microbit-coding-craft-project-book-microbit-in-wonderland.html)
- [Beginning BBC micro:bit](https://www.apress.com/gb/book/9781484233597)


## 教材

- [microbit.org の教材](https://www.microbit.org/teach/)
- [Code Club micro:bit projects](https://www.codeclubprojects.org/en-GB/microbit/)
- [Make with the micro:bit by Technology Will Save Us](http://make.techwillsaveus.com/bbc-microbit)
- [IET micro:bit Teaching Resources](http://microbit.org/teach/iet/) - とても成功している IET (Institution of Engineering and Technology) Faraday ブランドの一部で、IET 作成の一連の教材。
- [Grok Learning](https://groklearning.com/microbit/) - オンラインの MicroPython エディタや Blockly ビジュアルプログラミング、完全な micro:bit シミュレーター、カリキュラムに沿った教材、auto-marked 問題集。
- [micro:bit For Primary Schools](http://mb4ps.co.uk) - 小学校の教室用のカスタマイズ可能な作業と教材の計画。
- [101 Computing BBC micro:bit category](http://www.101computing.net/category/bbc-microbit/) - プログラミングスキルを向上させたり、コンピューターサイエンスの教え方に味付けする micro:bit 用のコンピューターチャレンジ。
- [micro:bit Maths](https://microbitmathsblog.wordpress.com) - 算数教育で BBC micro:bit を使う方法に関する記事。
- [micro:bit of Things](https://sites.google.com/view/microbitofthings/) - Key Stage 2(7-11歳) と 3(11-14歳) 向けの micro:bit プロジェクトのアイデアノート。
- [The Brooke Primary School Space Programme](http://www.brooke.norfolk.sch.uk/brooke-space-programme/) - Brooke Primary School の生徒の BBC micro:bit を宇宙に打ち上げる実験とセンサー計測を含んだプロジェクトに関する資料。
- [FunWithMicrobit](https://github.com/MicrobitPolska/FunWithMicrobit) - 子供たちによる子どもたちのための6時間のワークショップ FunWithMicrobit 。
- [Year 7 micro:bit lessons](http://www.jonwitts.co.uk/year-7-microbit) - micro:bit と Python を生徒に紹介するための授業。
- [UCL’s BBC Micro:bit Tutorials](http://microbit-challenges.readthedocs.io/en/latest/) - 生徒に問題に対するソリューションをデザインを始めさせる実践的な例とmicro:bit機能を紹介する解説一覧。
- [BBC micro:bit and Kodu Interact](http://www.kodugamelab.com/resources/#microbit) - miro:bit とやり取りできるゲーム開発用のビジュアルプログラミング言語 Kodu。
- [Build A Robot Wars Buggy](https://www.kitronik.co.uk/blog/robot-buggy-part-1-build-robot-wars-buggy-introduction/) - 先生向けにまとめられた、生徒に学期間または年間を通して学ばせる1つにまとまったデザインと技術チャレンジの楽しい学習教材。
- [CPC UCreate Micro:bit resources](http://warksjammy.blogspot.co.uk/2017/04/cpc-ucreate-microbit-resources-all-in.html) - CPC(?)用の micro:bit 教材のコレクション。
- [Year 7 BBC micro:bit topic](https://bournetocode.com/projects/7-CS-micro/) - Bourne Grammar 校の BBC micro:bit 授業。
- [Microsoft 14 Week Curriculum](https://makecode.microbit.org/courses/csintro) - 中学生向け(11-14歳)。コンピューターサイエンスのバックグラウンドが無い先生向けであり、「コンピューターサイエンス入門」を教えるときにも使える。
- [micro:bit in science teaching - How clean is my pond](https://community.computingatschool.org.uk/resources/5204) - 池の藻類の成長をモニターし、フィルターポンプのコントロールに micro:bit を使用する。
- [Inventorspace micro:bit category](https://invent.sparkfun.com/cwists/category#products=%5B8%5D) - 教室や学校、学区で実践できるプロジェクトがある SparkFun 提供のコミュニティ。
- [Kitronik Inventors Kit Resources](https://www.kitronik.co.uk/blog/kitronik-inventors-kit-resources) - micro:bit を使ったプログラミングやハードウェアインタラクションを始めるときの素晴らしい方法。LEDやモーター、LDRとコンデンサを使った12の実験を含む。
- [CLOQQ Activities](https://cloqq.com/newtomorrowtogether2017) ([more](https://cloqq.com/tecnologia?id=14777677)) - 種々の難易度、対象年齢、時間のアクティビティ。
- [Learn micro:bit](https://github.com/LearnToProgramRoanoke/Learn-microbit) - BBC micro:bit を使ったプログラミングを学ぶプログラミングコードと教材。
- [Micro:bit Lessons Aligned to Code.org's CS Fundamentals](http://microbit.org/teach/code-org-fundamentals/) - 小学校と幼稚園の生徒向けの、Code.orgのコンピューターサイエンス基本カリキュラムに沿った授業計画。
- [First steps in using micro:bits with PCs](http://community.computingatschool.org.uk/resources/5437/single) - micro:bit がUSB経由または無線経由でPCアプリケーションにデータを送信する方法に関する広範囲な記事。
- [Starting Computer Science with the BBC micro:bit](http://microbit.org/en/2018-01-19-train_the_trainer/) - はじめの一歩からゲームまで。10-14歳の生徒向けにデザインされたコンピューターサイエンスの教材。
- [Science Experiment Lessons](https://makecode.microbit.org/courses/ucp-science) - 中学生と高校生1年生ぐらいを対象にした、物理世界の力学と作用を深く理解するためにデザインされたた科学実験授業。
- [Part 1](https://microbit.hackster.io/kkristoff/micro-bit-basics-for-teachers-part-1-the-hardware-768229), [Part 2](https://microbit.hackster.io/monica/micro-bit-basics-for-teachers-part-2-javascript-blocks-6eaed5), [Part 3](https://microbit.hackster.io/monica/micro-bit-basics-for-teachers-part-3-micropython-c3fde0) 先生向けの micro:bit の基礎。micro:bit を教室え使いたくてもどこからはじめて良いかわからない先生向け。全部わかっちゃう！

### BBC提供の先生向け資料

- [Welcome to the micro:bit - Live Lesson](http://www.bbc.co.uk/programmes/articles/2M3H2YpKLsw2W8fC2ycHYSR/welcome-to-the-micro-bit-live-lesson) - 簡単なコードでゲーム、アニメーション、ロボットの作り方を学ぶ。
- [Doctor Who and the micro:bit - Live Lesson](http://www.bbc.co.uk/programmes/articles/3ydvd6mvhl89cHVJ7F2nmzf/doctor-who-and-the-micro-bit-live-lesson) - ドクター・フー（Who）のチームと協力して BBC のライブレッスンで TARDIS をコントロールするテストに BBC micro:bit を使う。
- [Strictly micro:bit - Live Lessons](http://www.bbc.co.uk/programmes/articles/49tjW0qR05wXrdpK7ZbGTbs/strictly-micro-bit-live-lesson) - コーディングの基本を解説する完全版の BBC ライブレッスン。Strictly Come Dancing（イギリスの社交ダンスコンペティション番組）のスターが出演、 BBC micro:bit について学ぶ。
- [micro:bit: Mission to Mars - Live Lesson](http://www.bbc.co.uk/programmes/articles/3d5Chvn8QBgdP1Z1d9GN9gx/micro-bit-mission-to-mars-live-lesson) - BBC micro:bit に関する最新のライブレッスンから星へ到達する話。コンピューターサイエンスが人間の宇宙探索にどう使われているのかを調査。
- [Tackle time and space with Doctor Who and the BBC micro:bit](http://www.bbc.co.uk/programmes/articles/GDNGTpkHJrDJSYMQJbH9f1/tackle-time-and-space-with-doctor-who-and-the-bbc-micro-bit) - 勇気とカンニングとコーディングの冒険をドクター・フー（Who）と一緒にやる話。
	- [Part 1: Mission Sonic](http://www.bbc.co.uk/programmes/articles/52yF6JCCn1X2L4HKBQtgWlP/doctor-who-and-the-micro-bit-mission-sonic) - ドクター・フー（Who）が考えているReality Bombから世界を救うアイデアはなにか？
	- [Part 2: Mission Decode](http://www.bbc.co.uk/programmes/articles/1tbvkWxx5vqQDmGnWMSLBJg/doctor-who-and-the-micro-bit-mission-decode) - ドクター・フー（Who）が Daleks から奇妙なデータを受信した。データのデコードを助けるのは君次第！
	- [Part 3: Mission Hack](http://www.bbc.co.uk/programmes/articles/1ZD3hYYBZVM5SDCVKH6vGfm/doctor-who-and-the-micro-bit-mission-hack) - 最後のミッションだ。ここをクリックして Dalek の宇宙船をハッキングして侵入しよう。

## コミュニティ

- [Official Slack Channel](http://tech.microbit.org/get-involved/where-to-find/) - チャットグループに参加するオンライン申込みフォーム。そこはmicro:bit コミュニティの人たちと議論したり会ったりできる素晴らしい場所。
- [`@microbit_edu` on twitter](https://twitter.com/microbit_edu)
- [`microbitfoundation` on Facebook](https://www.facebook.com/microbitfoundation)
- [micro:bit Python mailing list (archived)](https://github.com/ntoll/microbit_mailman_archive)
- [micro:bit Sri Lanka User Group](http://microbitslug.org)
- [Croatian Makers](http://izradi.croatianmakers.hr/bbc-microbit-uvodna-stranica/)
- [MakeCode Gitter](https://gitter.im/makecode-community/Lobby)


## その他いろいろ

- [micro:bit broadcast](https://microbit-broadcast.embeddedlog.com) - (更新停止中、アーカイブ状態) micro:bit の最新ニュース記事、プロジェクト、資料に関するニュースレター。
- [microbit.org Support](https://support.microbit.org) - 広範囲の内容を含むFAQや記事、解説がある、micro:bit 財団が提供するサポートページ。
- [Radiobit, a BBC Micro:Bit RF firmware](https://github.com/virtualabs/radiobit) - Micropython ベース専用のファームウェアでできた Radiobit、セキュリティ研究者が Nordic ShockBurst プロトコル、拡張 ShockBurst プロトコル、Bluetooth Smart Link Layer 経由でデータを盗聴、送受信する、また 及び生の 2.4GHz GFSK 復調データを盗聴するもの。
- [micro:bit Poster](https://www.element14.com/community/servlet/JiveServlet/downloadBody/87638-102-3-368412/microbit24x15.pdf) - Element14 コミュニティが micro:bit の主要機能と部品を解説を詳細かつ美しく描いたポスター（PDFファイル）。
- [Bluetooth troubleshooting guide](http://www.bittysoftware.com/troubleshooting.html) - micro:bit の Bluetooth 関連のよくあるものから稀な問題の解決方法。
- [Micro World Tour](https://microworldtour.github.io) - micro:bit がリリースされる以前は、ワールドワイド Python コミュニティに来る人はほとんどいなかった。micro:bit の冒険のための面白いコンテンツとアイデアが沢山ある。
- [Parent's Complete Guide To The BBC micro:bit](https://www.kitronik.co.uk/blog/parents-complete-guide-bbc-microbit/) - コーディングの経験が無くても、親が子供のコーディング勉強を積極的に助けられる無料の資料s。
- [BBC Micro:bit composer](https://scratch.mit.edu/projects/201592887/) - 作曲とそれに伴う micro:bit の MicroPython コード、Scratch 製のツール。

## License & Trademarks

[![CC0](http://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the authors have waived all copyright and related or neighbouring rights to this work.

This projects is not endorsed, sponsored or associated with the BBC. "BBC", "micro:bit", and their logos are trademarks of the BBC.
