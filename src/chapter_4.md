# 4. メモリ
* 少し高額になっても2枚以上の偶数枚をチャネルを分けて構成する
* 32GBモジュールが割安, 8GBはとても割高
* DDR4-2666とDDR4-3200、CPUに合うのはどっち？

## 少し高額になっても2枚以上の偶数枚をチャネルを分けて構成する
<a href="https://ja.wikipedia.org/wiki/Xeon" target="_blank">Wikipedia Xeon</a>  
Copper Lakeで6チャネルをサポート

<a href="https://ja.wikipedia.org/wiki/EPYC" target="_blank">Wikipedia EPYC</a>  
Romeで8チャネルサポート

入札は価格重視なので、パフォーマンス問題が気にならないのであれば１チャネルのみ実装もあり得る。ただし、導入後にパフォーマンス問題になる可能性が高い。枚数を変更しても見積もりを取るとあまり金額が変わらないケースはある。

## 32GBモジュールが割安, 8GBはとても割高
<a href="https://www.dell.com/ja-jp/work/shop/povw/poweredge-r6515" target="_blank">DELL R6515</a>  
2020年現在、16GBモジュールが32GBの次に割安なので、16GBで構成する  
48GB必要、という場合はとても難しい。8GB 6枚より16GB 3枚のほうが明らかに安い  

## DDR4-2666とDDR4-3200、CPUに合うのはどっち？
<a href="https://ja.wikipedia.org/wiki/EPYC" target="_blank">Wikipedia EPYC</a>  
DDR4-2666よりDDR4-3200のほうが高性能で少し価格が高いが、第一世代EPYCでは2666以上のクロックのものを取り付けても意味がない。
