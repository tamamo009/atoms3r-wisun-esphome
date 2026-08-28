# atoms3r-wisun-esphome
M5AtomS3R + ATOMIC Wi-SUN-A1 (BP35A1) を ESPHome 経由で Home Assistant に接続する設定例

Arduino 版サンプル（[rin-ofumi/wisun_arduino](https://github.com/rin-ofumi/wisun_arduino)）と同じキットを、Home Assistant向けに使う方向けです。単純に接続しているだけなのでM5AtomS3Rでの液晶表示や履歴等の機能はありません。

## 必要なもの

- [AtomS3R](https://www.switch-science.com/products/9915)
- [ATOMIC Wi-SUN-A1](https://www.switch-science.com/products/11323)
- [ROHM BP35A1](https://www.zaikostore.com/zaikostore/stockDetail?productIdOfHitotsukara=pr6714723)
- Bルート ID / パスワード
- [Home Assistant](https://www.home-assistant.io/)と[ESPHome](https://esphome.io/)

## 使い方

1. `secrets.yaml.example` をコピーして `secrets.yaml` を作る
2. Wi-Fi と Bルート認証を記入する（`secrets.yaml` は公開しない）
3. `atoms3r-broute.yaml` を ESPHome に読み込んで書き込む

Bルート通信には [esphome-broute](https://github.com/homy-newfs8/esphome-broute) を使っています。

UART は AtomS3R の GPIO6 (TX) と GPIO7 (RX) です。
