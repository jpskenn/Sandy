# Sandy（サンディ）

![Sandy keyboard](/assets/README/DSC_7947.jpeg)  

Sandy is a keyboard with key height optimization.

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

- 左右対称のキーレイアウト  
  [Jones](https://github.com/jpskenn/Jones)と同様の、2行目と3行目にずれのない、左右対称な、シンメトリカル ロースタッガードのレイアウトです。
  ![左右対称のキーレイアウト](/assets/README/DSC_8104.jpeg)

- キースイッチを立体的に配置  
  3段階の高さで、キースイッチを立体的に配置しています。
  ![キースイッチの高さ](/assets/README/DSC_7974.jpeg)

  平面上のキー配置だけでは最適化しきれない部分を、キーの位置に応じて高さを変え、立体的に配置することで補っています。  
  Jonesに比べて、ホームポジションから遠いキーへの打鍵しやすさが向上しています。

- 60%ケースと組み合わせられる  
  GH60型ケース互換のネジ穴を用意してあるので、市販のケースと組み合わせて使用できます。  
  ※詳しくはビルドガイドを参照

- 外部EEPROM搭載  
  Remapでたくさんのレイヤーを使用できます。

- オプション機能  
  以下のオプション機能を使用できます。

  - ロータリーエンコーダ
  - インジケータLED
  - アンダーグローLED

## レイアウト

### バリエーション

キーのバリエーションを含むレイアウトは以下の通りです。  
Ctrl（左）とEnter（右）にはキーサイズのバリエーションがあり、最下行の中央にはロータリーエンコーダを配置できます。
[![Keyboard Layout Editor: Sandy (DN0030)](/assets/README/layout.png)  
Keyboard Layout Editor: Sandy (DN0030)](http://www.keyboard-layout-editor.com/#/gists/c907e866d8f82b82a22b455e622b7301)

### キーの高さ

キーの高さはLow（0mm）, Middle（3.6mm）, High（8.6mm）の3段階で、以下のように配置されます。  
![キーの高さ](/assets/README/layout_height_map.png)

### 推奨キーマッピング

このレイアウトは、左右の手の運指を同じにするため、[SemiErgo Layout](https://github.com/mtei/SemiErgo_Layout)に準ずるキーマッピングで使用することを念頭に設計されています。  
つまり、一般的なロースタッガードレイアウトから、アルファ部の左手側Z行を左へ1キー、数字行の右手側を右側へ1キーずらしたものが、推奨キーマッピングとなります。

以下にSemiErgoを適用した推奨キーマッピングの例を示します。  
枠で囲った部分が、一般的なロースタッガードからの変更箇所です。
![SemiErgoを適用した推奨キーマッピング例](/assets/README/layout_SemiErgo_based_w_marking.png)
<small>💡ヒント：このキーマッピング例ではスペースキーをSandS（Space & Shift）にしているので、左右端のシフトキーを取り除いています。</small>

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

Sandyは複数基板を重ねるという手法で製作しているため、その技術的な制限や、製作工程を複雑にしすぎない配慮により、全てのスイッチをなめらかな高さ変化で配置できていません。  
そのため、高さ方向へ最適化しきれていない部分が残っています。  

## 参考事例

- [Genesis2.5](https://github.com/sekigon-gonnoc/Genesis2.5-doc)（[販売ページ](https://booth.pm/ja/items/1308005)  
  行ごとに高さと傾きを変えることができる自作キーボードキット。  

- [Thumbs Up!](https://www.thumbsup.shop)  
  カラムスタガをベースに親指や中央のキーを高くした設計の自作キーボードキット。

- [Kinesis Advantage series](https://kinesis-ergo.com/products/#keyboards)  
  ”エルゴノミクス”、”3Dキーボード”と言えばこれが思い浮かぶのはこれ。凹形状にキーが配置されている。

- [Microsoft Sculpt](https://www.microsoft.com/en/accessories/products/keyboards/sculpt-ergonomic-desktop)  
  ほんのり放射状に並んだキーと、中央部が高くなった形状。

- [Dactyl](https://github.com/adereth/dactyl-keyboard)  
  3Dプリンタで作る、スイッチを3D配置したキーボード。

- ["3D" キーキャップ](https://qiita.com/zk_phi/items/5680607118516413a0ba)  
  キーボードはそのままに、キーごとに高さを変えた3D形状のキーキャップ。MXスイッチ用。

- [Gravity Keycaps](https://note.com/yfuku_/n/n1fbba2e8f44c)  
  Choc用の3D形状キーキャップ。

## 開発経緯

### 元々の計画

当初（2021年1月ごろ）は、Chocスイッチを使用するキーボード、[Nora](https://github.com/jpskenn/Nora)の打鍵しやすさ向上を目的に、スイッチの配置を立体的に改修する計画でした。  
Choc用キーキャップには、行ごとに高さの異なるプロファイルのものが存在しません。すべてのキーが同じ形状になっているため、1行目の数字行や、ホームポジションから遠いキーへ指が届きにくくなります。  
その状況を改善するための改修計画でしたが、あまりモチベーションも上がらず、手をつけずに放置していました。  

### Sandy計画の始動

2022年12月の末ごろ、[SMKJのアドベントカレンダー](https://scrapbox.io/self-made-kbds-ja/アドベントカレンダー)を久しぶりに読み返しながら、様々なアイデアや取り組みについて思いをめぐらせていました。
そのとき、ふとした思いつきでJonesのキーキャップを部分的に背の高いものに入れ替えたところ、思いのほか打鍵しやすくなることに気がつきました。  

![Jonesのキーキャップを部分的に背の高いものに入れ替えたテスト機](/assets/README/jones_key_height_test.jpeg)  
奥：通常のJones，手前：一部のキーを入れ替えたJones

Cherryプロファイルをベースにして、`T` `Y`は倍ほどの高さのSAプロファイル、`G`や`Q`などは少しだけ背の高いKATプロファイルに交換しました。  
この時点では`左右のシフト`などをOEMプロファイルでほんの少し高くしようとしていますが、後にボツとなります。

これをきっかけとして、MXスイッチを使用するキーボード、[Jones](https://github.com/jpskenn/Jones)を改修する計画として復活することになりました。  

### ロードテスト

先ほどのテスト機を使い部分的にキーキャップを交換してどのキーを最適化の対象にするかを調べたり、スチレンボードにスイッチをのせたモックアップを作成して最適な高さを探ったりしました。（`0+2+2`は、ベースの0mmに対して、1段目が2mm、2段目も2mmの段差を意味するメモ）

![モックアップ](/assets/README/IMG_4881.jpeg)  

テスト機は、数字行をSAプロファイルへ、また、`T` `Y`をSAプロファイル1行目のキーに交換してさらに高くした最終形態になりました。  

![最終形のテスト機](/assets/README/IMG_4914.jpeg)

この形態をロードテストとして3ヶ月ほど使用し、日常的な使用で問題ないことを確認した上で基板の製作に取り掛かりました。
