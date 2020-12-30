
homubridge用 汎用ＦＡＮプラグイン （eneral purpose FAN plugin）

Homebridge：  https：//github.com/nfarina/homebridge

ＯＦＦ（0%） ⇔ ＬＯＷ（33%） ⇔ ＭＩＤＤＬＥ（66%） ⇔ ＨＩＧＨ（100%）

時計回り（CLOCKWISE） ⇔ 反時計回り（CLOCKWISE）

の設定が可能です。

NatureRemo Cloud API特化バージョン↓
https://github.com/mizuka-ninomae/homebridge-nature-remo-cloud-fan#readme


config.json 記入例
```js

  "accessories": [{
    "accessory": "cmd-fan",
    "name": "シーリングファン",
    "high_cmd": "/home/pi/homebridge-cmd-fan_sh/high_cmd.sh",
    "middle_cmd": "/home/pi/homebridge-cmd-fan_sh/middle_cmd.sh",
    "low_cmd": "/home/pi/homebridge-cmd-fan_sh/low_cmd.sh",
    "off_cmd": "/home/pi/homebridge-cmd-fan_sh/off_cmd.sh",
    "clockwise_cmd": "/home/pi/homebridge-cmd-fan_sh/clockwise_cmd.sh",
    "c_clockwise_cmd": "/home/pi/homebridge-cmd-fan_sh/c_clockwise_cmd.sh"
  },
  {
  ～
  }]
```

ファイルの場所を指定出来ていれば /home/pi/homebridge-cmd-fan_sh/ でなくて構いません。

設置した.shの中に、それぞれの命令を出すコマンドを記述してください。

テスト環境（testing environment）

・Raspberry Pi3

・Nature Remo 1ST generation

・どれが商品名か分からないこの商品 https://item.rakuten.co.jp/low-ya/fc03-g1003-100/?s-id=ph_pc_itemname
