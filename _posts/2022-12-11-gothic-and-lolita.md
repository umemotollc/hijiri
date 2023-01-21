---
layout: post
title:  "SUPERBACHBOY 3"
date:   2021-10-21 00:00:00 +0900
categories: concert
youtubeId: EKFb66A6bdM
---

"SUPERBACHBOY 3" (2021)
for cello, electronics, electronic bulletin boards, acceleration sensor and Super-Famicom-controllers.

Comp.: Yuri UMEMOTO / 梅本佑利
Cello: Kei YAMAZAWA / 山澤慧
Media Art and Engineering: Hijiri UMEMOTO / 梅本聖

Recorded at "Mind Tree Vol.7", Tokyo Concerts Lab., Tokyo, on 21th of October 2021
山澤慧「マインドツリー vol.7」で初演（東京コンサーツラボ、2021年10月21日）。

{% include youtubePlayer.html id=page.youtubeId %}

## アコースティックと電子音楽を組み合わせた、「チェロ vs. 観客」の対戦型音楽作品。

チェロの弓には、加速度センサーを搭載したマイコンを設置(Nordic nRF52833)。Bluetooth LEでPC(Macbook Pro)に信号を送り、チェロの弓の動きに合わせて攻撃パターンを変化させる。
他方、観客のゲームコントローラー(スーパーファミコンのコントローラー）はUSBキーボード(HID)との変換装置(ESP32-WROOM)を通してPCの入力に連動しており、A/Bなどのボタンの連打によって、相手を攻撃する。

攻撃と防御の様子は、LEDディスプレイにリアルタイムで表示される。

攻撃が成功するとチェロの演奏パターンが変化するよう楽譜で指定されている。ゲームオーバー時の演奏も、勝ち負けにより２通り用意されている。

### 使用したデバイス
- ESP32-WROOM-32E https://akizukidenshi.com/catalog/g/gM-15675/
- nRF52833 (compatible with micro:bit v.2)

### 作成したソフトウエア
- 後日掲載
