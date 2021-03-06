# サーバー見積もりリファレンス

サーバー見積もり作業は**手間がかかって儲けの少ない厄介な作業**です。  
本資料は主に小中規模で使用する仮想化用サーバー見積もりを**必要十分なスペックで素早く作成**するためのリファレンスです。

## 目次 兼 まとめ

### 1. [要件](./chapter_1.md)
* 必ず読む。
* 必要な条件を見極める。 ストレージはくどい説明を行っていないSASを選択する。

### 2. [筐体](./chapter_2.md)
* 必ず構成ガイドを読む。
* もう2ソケット筐体は選ばない。
* LOMを見よ
* 増設スロット
* ベゼルいらない。ケーブルマネージメントアームいらない。ラックレールはスライドする一番安いやつ。DVDもいらないケースあり。
* SAS 2.5インチベイのものを選択する。3.5インチは下火、種類が少ない、条件に合致しない。

### 3. [CPU](./chapter_3.md)
* 「コア数」を見る。ソケットやスレッド数ではない。
* コア数が多いから高額というわけではない
* 最新の世代を選択する
* 最低クロック数に注意

### 4. [メモリ](./chapter_4.md)
* 少し高額になっても2枚以上の偶数枚をチャネルを分けて構成する
* 32GBモジュールが割安, 8GBはとても割高
* DDR4-2666とDDR4-3200、CPUに合うのはどっち？

### 5．[ストレージ](./chapter_5.md)
* SAS10000rpm HDDで3-4台のハードウェアRAID5構成にする。
* RAIDカードのスペックをよく読み、hotswapハードウェアRAID 0,1,5サポートでキャッシュ1Mバイトを選択。
* Boot Optimizedストレージ（Dellのブート用SSDで10万+）、SD CARDブート、USBブート等メリットないので外す

