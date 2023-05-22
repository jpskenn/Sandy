# Sandy（サンディ）

![Sandy keyboard](/assets/README/DSC_7928.jpeg)  

Sandy is a Keyboard with key height optimization.

Layered PCB will make height differences for each key.
This covers the lack of optimization to physical key layout that only adjust x-y direction in a plane.

---

Sandyは、スイッチの配置を立体的にして高さ方向への最適化を加えた、左右対称レイアウトの60%キーボードです。  

平面上のキーレイアウトだけでは最適化しきれない部分を、キーの位置に応じてスイッチを配置する高さを変えることで補っています。

名前の由来は、立体的、つまり3Dという意味を込めて…

``` text
3D → スリーディー → さんディー → サンディ → Sandy
```

という言葉遊びで、Sandy（サンディ）に決まりました。

---

## 特徴

- 左右対称なキーレイアウト  
  [Jones](https://github.com/jpskenn/Jones)と同様の、2行目と3行目にずれのない、左右対称な、シンメトリカル ロースタッガードのレイアウトです。

- キースイッチを立体的に配置  
  平面上のキーレイアウトだけでは最適化しきれない部分を、キーの位置に応じてスイッチを配置する高さを変えることで補っています。
  Jonesに比べて、ホームポジションから遠いキーへの打鍵しやすさが向上しています。

- 60%ケースと組み合わせられる（GH60型ケース互換）

- 外部EEPROM搭載  
  Remapでたくさんのレイヤーを使用できます。

- オプション機能  
  以下のオプション機能を使用できます。

  - ロータリーエンコーダ
  - インジケータLED

## レイアウト

キーのバリエーションを含むレイアウトは以下の通りです。  
Ctrl（左）とEnter（右）は、1.25uまたは1.5uのバリエーション。  
最下行の中央には、ロータリーエンコーダを配置できます。
[![Keyboard Layout Editor: Sandy (DN0030)](/assets/README/layout.png)  
Keyboard Layout Editor: Sandy (DN0030)](http://www.keyboard-layout-editor.com/#/gists/c907e866d8f82b82a22b455e622b7301)

キーの高さはLow（0mm）, Middle（3.6mm）, High（8.6mm）の3段階で、以下のように配置されます。  
![キーの高さ](/assets/README/layout_height_map.png)

[SemiErgo Layout](https://github.com/mtei/SemiErgo_Layout)に準ずるキーマッピングで使用することを念頭において設計したレイアウトです。  
レガシーレイアウトの一般的なロースタガから、左手アルファ部のZ行と右手数字行を外側へ1キーずらしたレイアウトが、推奨されるレイアウトです。  

SemiErgoを適用したレイアウト例は以下のようになります。  
![SemiErgoを適用したレイアウト](/assets/README/layout_SemiErgo_based.png)
<small>注：スペースキーをSandS（＝Space & Shift）にしているので、左右端のシフトキーは取り除いてあります。</small>

## ビルドガイド

- 最新版
  - [Sandy（DN0030）](/docs/BuildGuide_DN0030.md)

- 試作版
  - [Sandy（DN0020）](/docs/BuildGuide_DN0020.md)
  - [Sandy v.0.1](/docs/BuildGuide_v0_1.md)

## SNSタグ

[#Sandy_kbd](https://twitter.com/search?q=%23Sandy_kbd)

## ギャラリー

![Sandy keyboard, v.0.1](/assets/README/DSC_7893.jpeg)  
v.0.1, Cherryプロファイルキーキャップ使用  

![Sandy keyboard, 試作2号機](/assets/README/DSC_7942.jpeg)  
v.0.1, KATプロファイルキーキャップ使用

![Sandy keyboard, キーの段差（Cherryプロファイル）](/assets/README/DSC_7902.jpeg)  
キーの段差（Cherryプロファイル）

![Sandy keyboard, キーの段差（KATプロファイル）](/assets/README/DSC_7936.jpeg)  
キーの段差（KATプロファイル）

![Sandy keyboard, キーの段差（横と後ろ](/assets/README/DSC_7943.jpeg)  
キーの段差（横）

## 残る課題

Sandyは複数基板を重ねるという手法で製作しているため、その技術的な制限や、製作工程を複雑にしすぎないため、全てのスイッチをなめらかな高さ変化で立体的に配置できていません。  
そのため、最適化しきれない部分が多く残っています。  

## 参考事例

- [Genesis2.5](https://github.com/sekigon-gonnoc/Genesis2.5-doc)（[販売ページ](https://booth.pm/ja/items/1308005)）
  行ごとに高さと傾きを変えることができる自作キーボードキット。  

- [Thumbs Up!](https://www.thumbsup.shop)  
  カラムスタガをベースに中央側のキーを高くした設計の自作キーボードキット。

- [Kinesis Advantage series](https://kinesis-ergo.com/products/#keyboards)
  ”エルゴノミクス”、”3Dキーボード”と言えばこれが思い浮かぶ。凹形状にキーが配置されている。

- [Microsoft Sculpt](https://www.microsoft.com/en/accessories/products/keyboards/sculpt-ergonomic-desktop)  
  ほんのり放射状に並んだキーと、中央部が高くなった形状。

- [Dactyl](https://github.com/adereth/dactyl-keyboard)  
  3Dプリンタで作る、スイッチを3D配置したキーボード。

- ["3D" キーキャップ](https://qiita.com/zk_phi/items/5680607118516413a0ba)  
  キーボードはそのままに、キーごとに高さを変えたキーキャップ。MXスイッチ用。

- [Gravity Keycaps](https://note.com/yfuku_/n/n1fbba2e8f44c)  
  Choc用のキーキャップ。

## 開発経緯

### 元々の計画

当初（2021年1月ごろ）は、Chocスイッチを使用するキーボード、[Nora](https://github.com/jpskenn/Nora)の打鍵しやすさ向上を目的に、スイッチの配置を立体的に改修する計画でした。  
Choc用キーキャップには、行ごとに高さの異なるプロファイルのものが存在しません。すべてのキーが同じ形状になっているため、1行目の数字行や、ホームポジションから遠いキーへ指が届きにくくなります。  
その状況を改善するための改修計画でしたが、あまりモチベーションも上がらず、手をつけずに放置していました。  

### Sandy計画の始動

2022年12月の末ごろ、[SMKJのアドベントカレンダー](https://scrapbox.io/self-made-kbds-ja/アドベントカレンダー)を久しぶりに読み返しながら、様々なアイデアや取り組みについて思いをめぐらせていました。
そのとき、ふとした思いつきでJonesのキーキャップを部分的に背の高いものに入れ替えたところ、思いのほか打鍵しやすくなることに気がつきました。  

![Jonesのキーキャップを部分的に背の高いものに入れ替えたテスト機](/assets/README/jones_key_height_test.jpeg)  
Jonesのキーキャップを部分的に背の高いものに入れ替えたテスト機  
奥：通常のJones，手前：一部のキーを入れ替えたJones
Cherryプロファイルをベースにして、`T` `Y`はSAプロファイル、`G`や`Q`などはKATプロファイルに交換しました。  
`左右シフト`や`Z`をOEMプロファイルで少し高くしようとしていましたが、後にボツとなります。

これをきっかけとして、MXスイッチを使用するキーボード、[Jones](https://github.com/jpskenn/Jones)を改修する計画として復活することになりました。  

### ロードテスト

中身はJonesのテスト機をSandyのv.0として、部分的にキーキャップを交換してどのキーを最適化の対象にするか、また、どの程度の段差が最適な高さになるのかを探っていきました。  

![最終形のテスト機](/assets/README/IMG_4914.jpeg)  
最終形のテスト機  
数字行をSAプロファイルへ、また、`T` `Y`をさらに高くするためSAプロファイル1行目のキーに交換しました。

テスト機を3ヶ月ほど使用し、日常的な使用で問題ないことを確認しました。

また、すべて同じプロファイルのキーキャップにしたときの使用感を確認するため、スチレンボードにスイッチをのせたモックアップも作成しました。

![モックアップ](/assets/README/IMG_4881.jpeg)  
モックアップ
`0+2+2`は、ベースの0mmに対して、1段目が2mm、2段目も2mmの段差を意味するメモ。
