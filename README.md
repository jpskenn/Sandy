# Sandy

a Keyboard with key height optimization

Layered PCB will make height differences for each key.
This covers the lack of optimization to physical key layout that only adjust vertical and horizontal in a plane.

For comfortable typing.
Easy to type keys far from home position.

Ex.

- "T" and "Y"
- R1 row, Numerics and Symbols
- R2 Mod keys

---

# Sandy（サンディー）とは

Sandyは、スイッチの高さ方向に最適化を加えた、左右対称レイアウトの60%キーボードです。  
Jonesの2行目と3行目にずれのない左右対称なロースタガレイアウトを元に、キーの位置に応じてスイッチを配置する高さを最適化することで、さらに快適に打鍵できます。（設計段階コメント：たぶん）

一般的なキーボードからの乗り換えでも違和感のないレイアウトと十分なキー数を持ちつつ、40%や50%キーボードのコンパクトで軽快な運指の心地良さを兼ね備えています。

GH60型やPoker型に互換性のあるケースや、専用のボトムプレートと組み合わせて使用できます。

名前の由来は、立体的、つまり3Dという意味を込めて…

``` text
3D → スリーディー → さんディー → サンディー → Sandy
```

という言葉遊びで、Sandy（サンディー）に決まりました。

---

## 目次

<!-- @import "[TOC]" {cmd="toc" depthFrom=2 depthTo=4 orderedList=false} -->

<!-- code_chunk_output -->

- [目次](#目次)
- [スイッチ配置の最適化手法と課題](#スイッチ配置の最適化手法と課題)
- [開発の目的や改善点](#開発の目的や改善点)
- [レイアウト](#レイアウト)
- [タグ](#タグ)
- [こぼれ話](#こぼれ話)
  - [先行事例](#先行事例)
  - [使用者の手にあわない3Dキーボードはつらい？](#使用者の手にあわない3dキーボードはつらい)
  - [元々の計画](#元々の計画)
  - [平面的なスイッチ配置とキーの大きさ](#平面的なスイッチ配置とキーの大きさ)

<!-- /code_chunk_output -->

## スイッチ配置の最適化手法と課題

一般的なキーボードは平面的にスイッチが配置されており、その配置を目的に応じて最適化したレイアウトを作成することで、打鍵のしやすさを改善させたり、疲れにくくするなどといった、打鍵感の向上への取り組みがおこなわれています。  
また、行ごとに高さの異なる形状（※）のキーキャップを使用することで、ホームポジションから遠いキーにも指が届きやすくしています。  
しかし、スイッチ配置の最適化が平面上にとどまるため、縦と横の2方向しか最適化できず、レイアウトの最適化には限界がありました。  
また、キーキャップの高さは行単位の変化のため、指の長さや、ホームポジションからの離れ具合に応じた最適化はおこなわれていません。  

<small>※形状  
キーの形状はプロファイルと呼ばれる。  
Cherry, OEM, SA, KAT, DSS, MT3などのプロファイルは、行ごとに高さの異なる形状。  
DSAやXDAなど、すべて同じ形状のプロファイルも存在する。  
参考：[Keycaps.info](https://www.keycaps.info)</small>

これらの問題を解決するため、スイッチを立体的に配置し、縦・横・高さの3方向へ最適化した3Dキーボードがあります。  
市販品では[Kinesis Advantage](https://kinesis-ergo.com/products/#keyboards)や[Microsoft Sculpt](https://www.microsoft.com/en/accessories/products/keyboards/sculpt-ergonomic-desktop)などがあり、最近では3Dプリンタで作る[Dactyl](https://github.com/adereth/dactyl-keyboard)なども出てきています。  
これらは非常に高度な最適化がおこなわれ、効果は抜群ですが、筐体サイズや独特のキー配置など一般的なキーボードから乗り換えづらい面があったり、3Dプリンタの使用や組み立て難易度が高く手を出しにくいところがありました。  

別方向からのアプローチとして、3D形状のキーキャップを使用する方法もあります。  
キーボードはそのままでキーキャップを取り替えるだけで3Dキーボードに近づけようとする取り組みで、最適化の範囲は限られますが、かなりの効果が期待できます。  
残念ながら、対応するキーボードが限られてしまうため、その恩恵を受けられるのはごくわずかでした。  
また、キーキャップのデザインや色のバリエーションが少なく、キーの刻印がないことも敬遠される理由となっていました。  
参考：  
["3D" キーキャップ](https://qiita.com/zk_phi/items/5680607118516413a0ba)  
[Gravity Keycaps](https://note.com/yfuku_/n/n1fbba2e8f44c)

## 開発の目的や改善点

一般的なキーボードは最適化が限定的であるため打鍵感の向上もそこそこのレベルにとどまっていましたが、その解決方法（3Dキーボードや3Dキーキャップなど）も、さまざまな事情で選択しにくいという状況でした。

そこで、一般的なキーボードとそれほど変わらないレイアウトのまま、スイッチ配置の高さ方向へ最適化を加えることを目標にしたキーボード、Sandyを開発しました。  
GH60型ケースに対応する60%キーボードとして使用することを念頭に、物理配列などの基本部分は、以前開発した[Jones](https://github.com/jpskenn/Jones)を元にしています。  

Jonesは、平面上のスイッチ配置を最適化して左右対称な独自配列のロースタガのレイアウトを作成することで、打鍵しやすさの向上を目指していました。  
Sandyでは、スイッチの配置を立体的にして高さ方向への最適化を加えることで、Jonesで最適化しきれなかった場所、特にJonesのレイアウトの制約（※）を受ける箇所に対して、打鍵感をさらに向上させることを目指します。

<small>※Jonesのレイアウトの制約  
Jonesは、一般的なロースタガのレイアウトから離れすぎないことや、数字行を含めた5行、60%相当のキー数をGH60型のケースに収めるといった特徴をもつため、基本的には横方向にしか最適化できないという制約があります。  
たとえば、独自のケースを使用する[Ergotonic49](https://hanachi-ap.github.io/ergotonic49_docs/)では、キーを傾けることも含め、縦と横の両方向へ最適化がおこなわれています。</small>

なお、技術的な制限や、製作工程を簡単にするため、全てのスイッチをなめらかな高さ変化で立体的に配置できていません。  
そのため、最適化しきれない部分が残り、3Dキーボードなどの最適化度合いには遠く及びません。  
しかし、一般的なキーボードと違いすぎない割に打鍵感が良いことや、使用できるキーキャップの選択肢が広いことなど、Sandyを選ぶ理由があると考えています。

## レイアウト

[Keyboard Layout Editor](http://www.keyboard-layout-editor.com/#/gists/1d0f4082c7ae670692987e3519c82648)（暫定）

## タグ

\#Sandy_kbd

## こぼれ話

### 先行事例

- [Genesis2.5](https://github.com/sekigon-gonnoc/Genesis2.5-doc)（[販売ページ](https://booth.pm/ja/items/1308005)）
  行ごとに高さと傾きを変えることができる自作キーボードキット。  

### 使用者の手にあわない3Dキーボードはつらい？

執筆中

### 元々の計画

当初（2021年1月ごろ）は、Chocスイッチを使用するキーボード、[Nora](https://github.com/jpskenn/Nora)の打鍵感向上を目的に改修する計画でした。  
その内容は、以下のようなChoc用キーキャップで打鍵感が低下する状況を改善するためのものでしたが、さまざまな理由により停止していました。  

> MX用キーキャップでは、行ごとに高さの異なるプロファイルのキーキャップ（Cherry, OEM, SA, KAT, DSS, MT3など）を使うことで、平面的なキーレイアウトに対して高さ方向の最適化がおこなわれ、ホームポジションから遠い1行目などのキーへも指が届きやすくなる。  
>  
> しかし、一般的なChoc用キーキャプはすべて同一のプロファイルのため、高さ方向の最適化がおこなわれず指が届きにくい状況が生じてしまい、打鍵感が低下する。

この計画は1年ほど停止していましたが、キーボードのレイアウト設計において、平面的にスイッチを配置する最適化方法に限界を感じていたことや、軽い気持ちでおこなった打鍵テストの結果が思いのほか良かったことなどから、MXスイッチを使用するキーボード、[Jones](https://github.com/jpskenn/Jones)を改修する計画として復活することになりました。  

![Jonesのキーキャップを部分的に背の高いものに入れ替えたテスト](/assets/README/jones_key_height_test.jpeg)  
Jonesのキーキャップを部分的に背の高いものに入れ替えたテスト  
奥：通常，手前：一部のキーを入れ替え

### 平面的なスイッチ配置とキーの大きさ

平面的にスイッチを配置する場合、スイッチの配置間隔をキーキャップの大きさ以下に狭められない（干渉する）ため、最適化の範囲が制限されます。  

立体的に配置する場合でもキーキャップの大きさによる影響を受けますが、スイッチを隣のキーの方へ向けて（x軸y軸に沿って回転して）配置できるため、キーの並びはキーキャップ天面の大きさまで狭めることができ、最適化の範囲がもう少し広くなります。  

どちらの場合でも、サイズの小さなキーキャップを使うことで、最適化の範囲を広くすることができます。  
関連：狭ピッチキーボード

### キーキャップの設計が悪い説

キーボード側で、指の長さや、ホームポジションからの離れ具合に応じた最適化をおこなう取り組みを紹介した。  
しかし、逆に考えれば、キーキャップ自体が、指の長さや、ホームポジションからの離れ具合に応じた高さになっていれば、3Dキーボードのような最適化度合いに及ばないとしても、平面的なキーボードはもっと打鍵しやすくなっていたのではないでしょうか？

Cherryプロファイルなどの設計者は、このキーの高さで打鍵しやすいのでしょうか？  
アジア系の僕の手が小さすぎる、ということもありますが。

### 手を筐体に沿わせる使いやすさ

Nikon F3、直線的。エルゴノミック云々以前の時代。  
Nikon F4、溶けたチョコレートのように、角が丸められ、すべてが曲線、曲面で構成されたような、いわゆるエルゴノミックな筐体デザイン。  
どちらも、ジョルジェット・ジウジアーロがデザインを担当。

F3は角ばった直線的な筐体デザインですが、持ちにくいとか、グリップしにくいということはなく、むしろ使いやすくも感じます。  
自分から、手をカメラ筐体に沿わせていくような印象があります。
もし直線的な部分が使いづらかったなら、プレス用のバリエーションも生まれなかったでしょうし、20年も売り続けなかったでしょう。その前に、買う人だっていなくなっていたことでしょう。

F4のつるっとしたデザインは、確かに手にフィットするような気がします。  
F3とは逆に、カメラの方から手の中に入ってくるような印象を受けます。
ですが、指に引っかかるところがないため、ある程度力を入れて握っていないと、手からスルッと逃げてしまうように感じます。長時間使い続けるときは、掴んでおこうと力んでしまって、余計に疲れてしまうように感じます。

キーボードのSandyも、キーの高さの変化はなめらかではなく、”段差”がついた角ばって直線的な並びになっています。  
F3のデザインのように、「なめらかではないけれど、それはそれで使いやすい」と感じられれば良いなぁと思っています。
