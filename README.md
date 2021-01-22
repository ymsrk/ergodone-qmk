# ergodone-qmk

### ergodoneにキーマップを書き込むための手順

```
$ git clone git@github.com:ymsrk/ergodone-qmk.git
$ cd ergodone-qmk
$ sh ./setup.sh
$ cd qmk_firmware
// qmk configuratorを利用して.hexファイルをqmk_firmwareに配置する。
$ cp {ergodone_xxxxxxxxxx.hex} .
// フラッシュモードに入るには、最初にキーボードを取り外します。次に、左側のデバイスの一番上の行で、キーボードを再接続する間、右端の2つのキーを押し続けます。
$ ../tkg-toolkit/mac/bin/hid_bootloader_cli -mmcu=atmega32u4 {ergodone_xxxxxxxxxx.hex}
```

#### フラッシュモードにするための手順
```
x のところを押した状態でPCに接続する。
Left Hand
┌┈┈┈┈┈┬┈┈┈┬┈┈┈┬┈┈┈┬┈┈┈┲━━━┳━━━┓
│     │   │   │   │   ┃ 𝘅 ┃ 𝘅 ┃
├┈┈┈┈┈┼┈┈┈┼┈┈┈┼┈┈┈┼┈┈┈╄━━━╇━━━┩
│     │   │   │   │   │   │   │
├┈┈┈┈┈┼┈┈┈┼┈┈┈┼┈┈┈┼┈┈┈┼┈┈┈┤   │
│     │   │   │   │   │   ├┈┈┈┤
├┈┈┈┈┈┼┈┈┈┼┈┈┈┼┈┈┈┼┈┈┈┼┈┈┈┤   │
│     │   │   │   │   │   │   │
└┈┬┈┈┈┼┈┈┈┼┈┈┈┼┈┈┈┼┈┈┈┼┈┈┈┴┈┈┈┘
  │   │   │   │   │   │
  └┈┈┈┴┈┈┈┴┈┈┈┴┈┈┈┴┈┈┈┘
```

#### 不明点があれば公式を確認  
[qmk_firmware/keyboards/ergodone/](https://github.com/qmk/qmk_firmware/tree/master/keyboards/ergodone)
（ただ、あまり情報はない。。。）

#### QMK Configurator

QMKにマージされたキーボードのキーマップをウェブ画面上から操作して新しいキーマップを作り、それをダウンロード出来るWebサービスです。
[QMK Configurator](https://config.qmk.fm/#/mechlovin/kanu/LAYOUT_all)
