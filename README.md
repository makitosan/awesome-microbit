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
- [書籍](#books)
- [教材](#teaching-resources)
- [コミュニティ](#community)
- [その他いろいろ](#miscellaneous)

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

MakeCode 周辺知識に不足しており駄目翻訳になりそうなので後回し :wink:

- [Neopixel](https://github.com/Microsoft/pxt-neopixel) - Neo-Pixel (individually addressable RGB LEDs) package.
- [Filesystem](https://github.com/Microsoft/pxt-filesystem) - BETA package to support file system.
- [MAX6675](https://github.com/Microsoft/pxt-max6675) - Package for the MAX6675 component in PXT.
- [Bluetooth MAX6675](https://github.com/Microsoft/pxt-bluetooth-max6675) - Bluetooth service for the MAX6675 temperature probe.
- [Sonar](https://github.com/Microsoft/pxt-sonar) - Microsoft MakeCode package to handle sonar sensors and pings.
- [Bluetooth Temperature Sensor](https://github.com/Microsoft/pxt-bluetooth-temperature-sensor) - Bluetooth service to expose a temperature reading.
- [MIDI](https://github.com/Microsoft/pxt-midi) - MIDI interface for MakeCode - beta.
- [Bluetooth MIDI](https://github.com/Microsoft/pxt-bluetooth-midi) - Bluetooth Midi package for Microsoft Make Code - beta.
- [BlueDot](https://github.com/Microsoft/pxt-bluedot) - PXT package to support the BlueDot app - beta.
- [GY521](https://github.com/PaulDFoster/pxt-microbit-GY521) - PXT package for the micro:bit to drive a MPU-6050 (GY-521).
- [UCL Junkrobot](https://github.com/chevyng/pxt-ucl-junkrobot) - Junk robot controlled using 28BYJ-48 stepper motors and HC-SR04 ultrasonic sensor.
- [BitBot](https://github.com/srs/pxt-bitbot) - BitBot Package for Microsoft PXT.
- [gamer:bit](https://github.com/sparkfun/pxt-gamer-bit) - SparkFun gamer:bit package for Microsoft MakeCode.
- [moto:bit](https://github.com/sparkfun/pxt-moto-bit) - MakeCode package for the SparkFun weather:bit board.
- [weather:bit](https://github.com/sparkfun/pxt-weather-bit) - Package to add support for the weather:bit add-on board from SparkFun.
- [SSD1306](https://github.com/Tinkertanker/pxt-ssd1306-microbit) - Package for SSD1306 OLED controller, based on the Adafruit Arduino library.
- [mi:node](https://github.com/minodekit/pxt-minode) - Mi:node kit (micro:bit IoT Starter Kit by element14) driver package.
- [Kitronik Servo Lite](https://github.com/KitronikLtd/pxt-kitronik-servo-lite) - Blocks that support Kitronik Servo:Lite board for the micro:bit.
- [Kitronik I2C 16 Servo](https://github.com/KitronikLtd/pxt-kitronik-I2C-16-servo) - Blocks for driving the Kitronik I2C 16 servo expansion board.
- [Kitronik motor driver](https://github.com/KitronikLtd/pxt-kitronik-motor-driver) - Blocks for driving the Kitronik micro:bit motor driver board.
- [Lego Power Functions](https://github.com/philipphenkel/pxt-powerfunctions) - Control your LEGO® Power Functions motors using your micro:bit with an infrared LED.
- [KY040](https://github.com/Tinkertanker/pxt-ky040-microbit) - Tinkertanker package for the KY-040 rotary encoder.
- [Invent robot](https://github.com/techcampuk/pxt-invent) - This library provides a Microsoft PXT package for Invent robot.
- [Robotbit](https://github.com/KittenBot/pxt-robotbit) - Package for KittenBot Robotbit.
- [ubirch NB-IoT](https://github.com/ubirch/pxt-ubirch) - Package for sending signed data messages to the ubirch backend.
- [CCS811](https://github.com/ADataDate/pxt-airQuality) - Makecode Package for the CCS811 Air Quality Sensor.
- [DS1307](https://github.com/Tinkertanker/pxt-ds1307-microbit) - Tinkercademy MakeCode package for using the DS1307 RTC (Real-Time Clock).
- [HT16K33](https://github.com/Tinkertanker/pxt-ht16k33-alnum4) - Tinkercademy MakeCode Package for the HT16K33 I2C Alphanumeric Display (beta).
- [HoneyBit](https://github.com/HoneycombKits/pxt-HoneyBit) - A Honeycomb kits package for micro:bit MakeCode.
- [katakana](https://github.com/mbitfun/pxt-katakana) - This library make it possible to show characters of Katakana in half-width.
- [Bluetooth beacons](https://github.com/kshoji/pxt-bluetooth-beacons) - Allows the micro:bit to act as iBeacon / AltBeacon advertiser.
- [micro turtle](https://github.com/Microsoft/pxt-microturtle) - A LOGO-like turtle library, the turtle is a single pixel moving on the micro:bit screen.
- [Grove](https://github.com/seeed-studio/pxt-grove) - Blocks for several Seeed Studio Grove modules.
- [LumexOLED](https://github.com/lioujj/pxt-oled) - Package designed for Lumex OLED display.

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

### Project Collections

- [microbit.co.uk Site Index](https://www.microbit.co.uk/index) - The microbit.co.uk website contains an extensive list with all their projects and tutorials.
- [hackster micro:bit community](https://microbit.hackster.io) - This hackster community contains user submitted projects for the micro:bit.
- [MakeCode Projects](https://makecode.microbit.org/projects/) - List of micro:bit projects you can do with the MakeCode editor.
- [Inventorspace micro:bit category](https://invent.sparkfun.com/cwists/category#products=%5B8%5D) - Community by SparkFun with fun projects you can implement in your classroom, school or district.
- [Tinkercademy Projects](https://tinkercademy.com/microbit/) - Collection of projects using the micro:bit and Tinkercademy Tinker Kit.
- [Raspberry Pi micro:bit Projects](https://projects.raspberrypi.org/en/projects?technologies%5B%5D=microbit) - Collection of Raspberry Pi and micro:bit projects from the Raspberry Pi Foundation.
- [Hackaday.io micro:bit Projects](https://hackaday.io/projects?tag=micro%3Abit) - Projects using the micro:bit tag in Hackaday.io, a collaborative hardware development community.


## 記事

Useful Articles for developing on the micro:bit.

- [Offline C/C++ Development With The Micro:bit](http://www.i-programmer.info/programming/hardware/9654-offline-cc-development-with-the-microbit-.html)
- [Sending 'commands' from a micro:bit over Bluetooth](http://bluetooth-mdw.blogspot.co.uk/2016/07/sending-commands-from-microbit-over.html)
- [Modelling micro:bit data with the Bitty Data Logger App](https://www.stem.org.uk/elibrary/community-resource/289686/modelling-microbit-data-bitty-data-logger-app)
- [Getting Started with the micro:bit Bluetooth IO Pin Service](https://ukbaz.github.io/howto/ubit_ble_profile.html)
- [Using MQTT-SN over BLE with the BBC micro:bit](https://blog.benjamin-cabe.com/2017/01/16/using-mqtt-sn-over-ble-with-the-bbc-microbit)
- [The First Video Game on the BBC Micro:bit [probably]](https://hackernoon.com/the-first-video-game-on-the-bbc-micro-bit-probably-4175fab44da8) - Creating a game for the micro:bit, the MicroPython changes needed to increase performance and a general profile of its resources.
- [Custom BLE services with micro:bit](https://www.hackster.io/pelikhan/custom-ble-services-with-micro-bit-6c9879) - Build your own Bluetooth low energy services and bundle them as PXT/MakeCode blocks that beginners can use.
- [Excel and Micro:Bit - Hacking for fun and creativity!](https://techcommunity.microsoft.com/t5/Excel-Blog/Excel-and-Micro-Bit-Hacking-for-fun-and-creativity/ba-p/63603) - Experiment to have some basic sensor data collected using the micro controller and then visualized in Excel.
- [Writing the second video game for the Micro:bit in Rust](https://hackernoon.com/writing-the-second-video-game-for-the-micro-bit-in-rust-3cd8b5ab22d3) - Updating a micro:bit game and porting it to the Rust language.
- [Adding a new module to MicroPython](http://cigdemsengul.blogspot.co.uk/2017/04/offline-development-in-microbit-adding.html) - Article describing an experiment to add a new module into MicroPython for the micro:bit.
- [Become a Time Lord with the BBC micro:bit](https://blog.groklearning.com/become-a-time-lord-with-the-bbc-micro-bit-c4b8b4e2d747) - Using different timing mechanisms to run multiple things in MicroPython.
- [Debugging the micro:bit with pyOCD and GDB](https://docs.mbed.com/docs/mbed-os-handbook/en/5.4/debugging/debugging_microbit/) - Shows how to debug a micro:bit program using PyOCD and GDB.
- [Exploring the BBC micro:bit Software Stack](http://mattwarren.org/2017/11/28/Exploring-the-BBC-microbit-Software-Stack/) - What’s in it, what it does and how it all fits together.
- [Building the 1,000 BBC micro:bit Display](https://www.kitronik.co.uk/blog/building-the-bbc-microbit-matrix-display/) - Is it possible to build a screen to show images from a thousand BBC micro:bits?
- [micro:bit Radio Packets](https://ukbaz.github.io/howto/ubit_radio.html) - Explanation of the MakeCode radio packet specification (built on top of the micro:bit runtime specification) and how to communicate between MakeCode and MicroPython programs via radio.
- [Synchronized Music on micro:bits](https://blog.flowblok.id.au/2018-02/synchronized-music-on-microbits.html) - Building a micro:bit mesh network so they can play music synchronized across a large area.
- [Using the Built-in Sensors](https://learn.adafruit.com/micro-bit-lesson-1-using-the-built-in-sensors) - Learn how to use the micro:bit's built-in accelerometer and magnetometer.

### Article Collections

- [MultiWingSpan](http://www.multiwingspan.co.uk/micro.php) - Large collection of examples, instructions, and direction on how to use electronic components.
- [ElecFreaks micro:bit category](https://www.elecfreaks.com/blog/micro-bit/) - ElecFreaks collection of experiments going through the concepts of using individual sensors or components.
- [SparkFun micro:bit tutorials](https://learn.sparkfun.com/tutorials/tags/microbit) - Collection of tutorials from SparkFun, including comprehensive experiment guides for their kits.
- [BitIO blogs](http://warksjammy.blogspot.co.uk/2017/07/bitio-blogs-in-one-place.html) - Collection of blogs written about using the BitIO Python module to control the micro:bit.
- [micro:bit learning](http://www.microbitlearning.com/tag/microbit) - Blog with a section for articles showing how to use a wide selection of sensors with the micro:bit and the Arduino software.
- [Adafruit Learn micro:bit section](https://learn.adafruit.com/category/micro-bit) - Adafruit Learning System section for the BBC micro:bit.
- [BBC micro:bit - Kitronik University](https://www.kitronik.co.uk/blog/bbc-microbit-kitronik-university/) - A varied collection of micro:bit resources by Kitronik.


## 動画

- [MicroMonsters](https://www.youtube.com/channel/UCK2DviDexh_Er2QYZerZyZQ) - YouTube channel with tutorials to learn to code with your family.
- [micro:bit and Bluetooth](https://www.youtube.com/playlist?list=PLYOCnwH2UtBzhJ2nvn_DM3itz6GNVwrDu) - YouTube playlist with Martin Woolley's Bluetooth videos.
- [Video Series from The Maker Movies](https://www.youtube.com/playlist?list=PLD0HD_3AJljXDWoasq2x5gHmkKeV7cc-P) - List of short, introductory videos for anyone wanting to get started with the micro:bit.
- [SparkFun video resources](http://sparkfuneducation.com/video-resources/microbit.html) - Growing list of video resources for the micro:bit.
- [SamCodes YouTube Playlist](https://www.youtube.com/playlist?list=PLumNlyd5JxxegaAVScP7Qm1AXPtJdGBCq) - Video tutorials showing how to  use different electronic components and features of the micro:bit.
- [Fun with Zephyr Project and BBC micro:bit](https://www.youtube.com/watch?v=ZZRbIpVJGns) - This presentation shows how Zephyr empowers the BBC micro:bit devices and its Bluetooth chip to do fun things.


## Books

- [micro:bit IoT In C](http://www.iot-programmer.com/index.php/books/micro-bit-iot-in-c)
- [Programming with MicroPython](http://shop.oreilly.com/product/0636920056515.do)
- [Getting Started with the micro:bit](http://shop.oreilly.com/product/0636920115267.do)
- [The Official BBC micro:bit User Guide](https://www.wiley.com/en-gb/The+Official+BBC+micro:bit+User+Guide+-p-9781119386735)
- [Programming the BBC micro:bit](http://simonmonk.org/prog-mb/)
- [Networking with the micro:bit (ebook)](https://microbit.nominetresearch.uk/networking-book/)
- [micro:bit in Wonderland](http://www.techagekids.com/2017/11/our-beginner-bbc-microbit-coding-craft-project-book-microbit-in-wonderland.html)
- [Beginning BBC micro:bit](https://www.apress.com/gb/book/9781484233597)


## Teaching Resources

- [microbit.org Teaching Resources](https://www.microbit.org/teach/)
- [Code Club micro:bit projects](https://www.codeclubprojects.org/en-GB/microbit/)
- [Make with the micro:bit by Technology Will Save Us](http://make.techwillsaveus.com/bbc-microbit)
- [IET micro:bit Teaching Resources](http://microbit.org/teach/iet/) - A series of resources created by the IET (Institution of Engineering and Technology) as part of their highly successful IET Faraday brand.
- [Grok Learning](https://groklearning.com/microbit/) - Provides an online MicroPython code editor, Blockly visual programming, full micro:bit simulator, curriculum-aligned teaching material and auto-marked problems.
- [micro:bit For Primary Schools](http://mb4ps.co.uk) - Fully-customisable scheme of work and resources for use in the primary classroom.
- [101 Computing BBC micro:bit category](http://www.101computing.net/category/bbc-microbit/) - Computing challenges with the micro:bit to boost your programming skills or spice up your teaching of computer science.
- [micro:bit Maths](https://microbitmathsblog.wordpress.com) - Blog exploring the BBC micro:bit in mathematics education.
- [micro:bit of Things](https://sites.google.com/view/microbitofthings/) - Notes on micro:bit project ideas for Key Stage 2 and 3.
- [The Brooke Primary School Space Programme](http://www.brooke.norfolk.sch.uk/brooke-space-programme/) - Project page documenting Brooke Primary School pupil's upcoming journey for launching a BBC micro:bit (on its own) into near-space, with experiments and sensor measurements.
- [FunWithMicrobit](https://github.com/MicrobitPolska/FunWithMicrobit) - FunWithMicrobit is a 6 hours workshop made by kids for the kids.
- [Year 7 micro:bit lessons](http://www.jonwitts.co.uk/year-7-microbit) - Lessons used to introduce students to the micro:bit and Python.
- [UCL’s BBC Micro:bit Tutorials](http://microbit-challenges.readthedocs.io/en/latest/) - Tutorial sheets that introduce micro:bit features with practical examples provided to invite students to design solutions to problems.
- [BBC micro:bit and Kodu Interact](http://www.kodugamelab.com/resources/#microbit) - Kodu is a visual programming language made specifically for creating games and allow interaction with the micro:bit.
- [Build A Robot Wars Buggy](https://www.kitronik.co.uk/blog/robot-buggy-part-1-build-robot-wars-buggy-introduction/) - This fun learning resource has been put together to provide teachers with an all in one design and technology challenge that you can set for your students over the course of a term or a year.
- [CPC UCreate Micro:bit resources](http://warksjammy.blogspot.co.uk/2017/04/cpc-ucreate-microbit-resources-all-in.html) - Collection of micro:bit resources made for CPC.
- [Year 7 BBC micro:bit topic](https://bournetocode.com/projects/7-CS-micro/) - BBC micro:bit lessons from Bourne Grammar school.
- [Microsoft 14 Week Curriculum](https://makecode.microbit.org/courses/csintro) - Targeted to middle school grades 6-8 (ages 11-14 years). It is also written for teachers who may not have a Computer Science background, or may be teaching an "Intro to CS" for the first time.
- [micro:bit in science teaching - How clean is my pond](https://community.computingatschool.org.uk/resources/5204) - Using a micro:bit to monitor the level of algal growth in a pond and to control a filter pump.
- [Inventorspace micro:bit category](https://invent.sparkfun.com/cwists/category#products=%5B8%5D) - Community by SparkFun with fun projects you can implement in your classroom, school or district.
- [Kitronik Inventors Kit Resources](https://www.kitronik.co.uk/blog/kitronik-inventors-kit-resources) - A a great way to get started with programming and hardware interaction with the microbit. Includes 12 experiments using LEDs, motors, LDRs and capacitors.
- [CLOQQ Activities](https://cloqq.com/newtomorrowtogether2017) ([more](https://cloqq.com/tecnologia?id=14777677)) - Activities with different difficulty levels, target age, and duration.
- [Learn micro:bit](https://github.com/LearnToProgramRoanoke/Learn-microbit) - Code and materials for learning to program with the BBC micro:bit.
- [Micro:bit Lessons Aligned to Code.org's CS Fundamentals](http://microbit.org/teach/code-org-fundamentals/) - Includes lesson plans aligned to Code.org's Computer Science Fundamentals curriculum for primary and elementary school students.
- [First steps in using micro:bits with PCs](http://community.computingatschool.org.uk/resources/5437/single) - This very comprehensive article explores ways in which the micro:bit can send data via USB cable or wirelessly to PC applications.
- [Starting Computer Science with the BBC micro:bit](http://microbit.org/en/2018-01-19-train_the_trainer/) - From Getting Started to Games. Computer Science teaching resources designed for use with students aged 10-14 years.
- [Science Experiment Lessons](https://makecode.microbit.org/courses/ucp-science) - Geared for students in middle and early high school, these Science Experiment lessons are designed help gain a greater understanding of the forces and behaviour of the physical world.
- [Part 1](https://microbit.hackster.io/kkristoff/micro-bit-basics-for-teachers-part-1-the-hardware-768229), [Part 2](https://microbit.hackster.io/monica/micro-bit-basics-for-teachers-part-2-javascript-blocks-6eaed5), and [Part 3](https://microbit.hackster.io/monica/micro-bit-basics-for-teachers-part-3-micropython-c3fde0) of micro:bit Basics for Teachers - Are you a teacher who wants to use micro:bit in your classroom, but doesn't know where to start? We'll show you how!

### BBC Teaching Resources

- [Welcome to the micro:bit - Live Lesson](http://www.bbc.co.uk/programmes/articles/2M3H2YpKLsw2W8fC2ycHYSR/welcome-to-the-micro-bit-live-lesson) - Learn how to create games, animations and robots using simple code.
- [Doctor Who and the micro:bit - Live Lesson](http://www.bbc.co.uk/programmes/articles/3ydvd6mvhl89cHVJ7F2nmzf/doctor-who-and-the-micro-bit-live-lesson) - The BBC micro:bit will be put to the test at the controls of the TARDIS in this special BBC Live Lesson in collaboration with the team behind Doctor Who.
- [Strictly micro:bit - Live Lessons](http://www.bbc.co.uk/programmes/articles/49tjW0qR05wXrdpK7ZbGTbs/strictly-micro-bit-live-lesson) - The full BBC Live Lesson exploring the basics of coding, with help from the stars of Strictly Come Dancing and the BBC micro:bit.
- [micro:bit: Mission to Mars - Live Lesson](http://www.bbc.co.uk/programmes/articles/3d5Chvn8QBgdP1Z1d9GN9gx/micro-bit-mission-to-mars-live-lesson) - Reach for the stars with our latest Live Lesson on the BBC micro:bit, which investigates how computer science can be used to aid man's exploration of space.
- [Tackle time and space with Doctor Who and the BBC micro:bit](http://www.bbc.co.uk/programmes/articles/GDNGTpkHJrDJSYMQJbH9f1/tackle-time-and-space-with-doctor-who-and-the-bbc-micro-bit) - Join The Doctor on an adventure of courage, cunning and coding!
	- [Part 1: Mission Sonic](http://www.bbc.co.uk/programmes/articles/52yF6JCCn1X2L4HKBQtgWlP/doctor-who-and-the-micro-bit-mission-sonic) - What plan does the Doctor have in mind to save the Universe from the Reality Bomb?
	- [Part 2: Mission Decode](http://www.bbc.co.uk/programmes/articles/1tbvkWxx5vqQDmGnWMSLBJg/doctor-who-and-the-micro-bit-mission-decode) - The Doctor has intercepted some seriously strange data from the Daleks; it's up to you to help decode it.
	- [Part 3: Mission Hack](http://www.bbc.co.uk/programmes/articles/1ZD3hYYBZVM5SDCVKH6vGfm/doctor-who-and-the-micro-bit-mission-hack) - It's the final mission! Click here to get hacking and infiltrate the Dalek spaceship.


## Community

- [Official Slack Channel](http://tech.microbit.org/get-involved/where-to-find/) - Online form to join this chat group, a great place to discuss and meet more people from the micro:bit community.
- [`@microbit_edu` on twitter](https://twitter.com/microbit_edu)
- [`microbitfoundation` on Facebook](https://www.facebook.com/microbitfoundation)
- [micro:bit Python mailing list (archived)](https://github.com/ntoll/microbit_mailman_archive)
- [micro:bit Sri Lanka User Group](http://microbitslug.org)
- [Croatian Makers](http://izradi.croatianmakers.hr/bbc-microbit-uvodna-stranica/)
- [MakeCode Gitter](https://gitter.im/makecode-community/Lobby)


## Miscellaneous

- [micro:bit broadcast](https://microbit-broadcast.embeddedlog.com) - (Discontinued, archived) newsletter to stay up-to-date with the latest micro:bit news, articles, projects, and resources.
- [microbit.org Support](https://support.microbit.org) - The support pages from the micro:bit Foundation is a great source of information, containing an extensive collection of FAQs, articles, and guides.
- [Radiobit, a BBC Micro:Bit RF firmware](https://github.com/virtualabs/radiobit) - Radiobit is composed of a dedicated Micropython-based firmware and a set of tools allowing security researchers to sniff, receive and send data over Nordic's ShockBurst protocol, Enhanced ShockBurst protocol, Bluetooth Smart Link Layer and sniff raw 2.4GHz GFSK demodulated data.
- [micro:bit Poster](https://www.element14.com/community/servlet/JiveServlet/downloadBody/87638-102-3-368412/microbit24x15.pdf) - Element14 has put together this detailed, beautifully rendered, cross-section micro:bit poster highlighting all of the device's key functions and components.
- [Bluetooth troubleshooting guide](http://www.bittysoftware.com/troubleshooting.html) - Tips on how to solve common and not so common micro:bit Bluetooth problems.
- [Micro World Tour](https://microworldtour.github.io) - Before the micro:bit was released a few went on a tour to the world-wide Python community. A lot of interesting content and ideas on these micro:bit adventures.
- [Parent's Complete Guide To The BBC micro:bit](https://www.kitronik.co.uk/blog/parents-complete-guide-bbc-microbit/) - Free resource to help parent's get actively involved in helping their children learn how to code, even with no prior coding experience.
- [BBC Micro:bit composer](https://scratch.mit.edu/projects/201592887/) - Write music and get the corresponding micro:bit micropython code, a tool made with Scratch.


## License & Trademarks

[![CC0](http://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the authors have waived all copyright and related or neighbouring rights to this work.

This projects is not endorsed, sponsored or associated with the BBC. "BBC", "micro:bit", and their logos are trademarks of the BBC.
