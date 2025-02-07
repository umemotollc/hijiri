---
layout: post
title:  "SUPERBACHBOY 3"
date:   2021-10-21 00:00:00 +0900
categories: concert
youtubeId: EKFb66A6bdM
---

## アコースティックと電子音楽を組み合わせた、「チェロ vs. 観客」の対戦型音楽作品。

"SUPERBACHBOY 3" (2021)  
for cello, electronics, electronic bulletin boards, acceleration sensor and Super-Famicom-controllers.


- Comp.: Yuri UMEMOTO / 梅本佑利
- Cello: Kei YAMAZAWA / 山澤慧
- Media Art and Engineering: Hijiri UMEMOTO / 梅本聖

Recorded at "Mind Tree Vol.7", Tokyo Concerts Lab., Tokyo, on 21th of October 2021

山澤慧「マインドツリー vol.7」で初演（東京コンサーツラボ、2021年10月21日）。

{% include youtubePlayer.html id=page.youtubeId %}



## 弦楽器用モーションセンサ、ワイヤレス・コントローラ及びこれらと連動するLEDパネルを備えた対戦型ゲームシステム

### チェロ用デバイス

チェロの弓には、加速度センサーを搭載したマイコンを設置(Nordic nRF52833)。Bluetooth LEでPC(Macbook Pro)に信号を送り、チェロの弓の動きに合わせて攻撃パターンを変化させる。

#### 制作のヒント

nRF52あるいは51を搭載したBLEモジュールを使うと簡単に実現できます。とくに、micro:bitはジャイロセンサを搭載しているので、電源と弓の取り付け方法を工夫すれば、比較的すくない工数で作ることができます。

- micro:bitにはモーションセンサが搭載されているので、センサの１軸を読み出す。
- センサの値の変化に応じて、BLE HIDでワイヤレスキーボードに値を出力。
 - 例えば、ボーイングのアップとダウンのゆるやかな１往復で、キーボードの「L」を出力。高速な１往復で「H」を出力するなど。あるいは、マウスとして連続した値の変化を送信する方法もある。
- コイン電池（CR2032など）で動作するように、３V給電にするとよい。
 - 秋月電子通商 [micro:bit用CR2032電源基板モジュール](https://akizukidenshi.com/catalog/g/g115442/)
 - スイッチエデュケーション [micro:bitバングルモジュールキット](https://switch-education.com/products/microbit-bangle-module-kit/)

### 観客用デバイス

観客のゲームコントローラー(スーパーファミコンのコントローラー）はワイヤレスでPCと接続されており、コントローラーのA/Bなどのボタンの連打によって、相手を攻撃する。コントローラーは、マイコン(ESP32-WROOM)を組み込んだカセットと接続されており、Bluetoothキーボートとして動作する。

攻撃と防御の様子は、LEDディスプレイにリアルタイムで表示される。

攻撃が成功するとチェロの演奏パターンが変化するよう楽譜で指定されている。ゲームオーバー時の演奏も、勝ち負けにより２通り用意されている。

### 使用したデバイス
- ESP32-WROOM-32E https://akizukidenshi.com/catalog/g/gM-15675/
- nRF52833 (compatible with micro:bit v.2)
- スーパーファミコン・コントローラー（初期ロット、無改造）
- LEDパネル（WS2812B互換プロトコル）
- LEDコントロール回路(FPGA)
 
### 作成したソフトウエア
- ソースコードが行方不明。そのうち再製します。
