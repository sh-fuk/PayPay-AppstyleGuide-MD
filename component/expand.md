# Expand

## Usage
* 情報量の多いコンテンツをコンパクトに表示する際に使用します
* エキスパンド内に情報を収めることで情報が整理され、下に続くコンテンツの可読性を高めます
* エキスパンドの利用は主コンテンツには使用せず、補足情報などの副次的な情報にのみ使用します
* タップすることで折りたたまれた情報を展開します
* 展開された情報は再度タップすることで展開前の状態に戻すことが可能です

### Usage Example
![情報量の多い副次的なコンテンツを折りたたんで表示](https://developer.paypay.ne.jp/static/img/expand_01.b0ad806c.png)

## Type
Expandのコンポーネントには3種類があり、用途によって使い分けをします。

![Card](https://developer.paypay.ne.jp/static/img/expand_02.f9a4797e.svg)
![List](https://developer.paypay.ne.jp/static/img/expand_03.e888bcc5.svg)
![Article](https://developer.paypay.ne.jp/static/img/expand_04.fa65ad06.svg)

## Detail

### Card
情報量の多いコンテンツをグルーピングする際に利用します。

![Cardに1-2の番号のマークアップがされてる画像](https://developer.paypay.ne.jp/static/img/expand_05.c7ef4da7.svg)

1 : 展開前 : タップで展開することを明示するため、下向きの矢印アイコンを表示します。Defaultの表示は閉じた状態を使用することを推奨します。展開後に表示される情報が想起可能なテキストラベルを表示します。
2 : 展開後 : 展開前の状態に戻せることを明示するため、上向きの矢印アイコンを表示します。

### List
リスト内の項目が多い場合、リストの一覧性を確保するために使用します。
情報を大項目、小項目に分類できるコンテンツにのみ使用可能です。

![Listに3-4の番号のマークアップがされている画像](https://developer.paypay.ne.jp/static/img/expand_06.31509d8f.svg)

3 : 展開前 : 大項目を表示します
タップで展開することを明示するため、下向きの矢印アイコンを表示します
Listの場合、ユーザーはExpandアクションを見逃す恐れがあります
1つ目の項目のみ、展開後の状態で表示することを推奨します
ただし、展開後の小項目が1st view内に収まらないほど多い場合はアクションがより不明瞭になるため、展開後のUIをDefault表示します

4 : 展開後 : 小項目を表示します
展開前の状態に戻せることを明示するため、上向きの矢印アイコンを表示します

### Article
記事などの長文コンテンツをコンパクトに表示する際に使用します。
情報を折りたたむことで下に続くコンテンツやアクションコンポーネントの可読性を高めます

![Articleに5-6の番号のマークアップがされている画像](https://developer.paypay.ne.jp/static/img/expand_07.12444228.svg)

5 : 展開前 : タップで展開することを明示するため、「続きを読む」などのテキストラベルを表示します
記事本文のテキストと混同しないよう、本文より弱い色を指定します
記事本文は、最終行の文字を…で省略します
省略位置は端末の横幅に準拠します

6 : 展開後 : 折りたたまれたコンテンツをすべて表示します
展開前の状態に戻すアクションは付与しません
リロードすると展開前の状態に戻ります

## Interaction
Expand areaをタップして、展開前/展開後のUIを切り替えます。
タップ時にはタップフィードバックを表示します。
Specを参照してください。

参考：[Interaction](../globalrule/interaction.md)

展開時は展開されるコンテンツ部分、矢印アイコンにアニメーションを付与し、状態の変化をわかりやすくします。

## Spec

### Card

![Cardに余白などのpx数がマークアップされている画像](https://developer.paypay.ne.jp/static/img/expand_08.ebee0da2.svg)
タップ領域を十分に確保します。

Text Label : 
[Heading / Label 14](../globalrule/typography.md)
Text Align-Center
Default > #00B9F5
Pressed( iOS ) > #00B9F5, Alpha 0.7

Background :
Default >
Background > #FFFFFF
Pressed( iOS ) >
Background > #F2F2F2

Icon : Icon

### Expand List

![Expandに余白などのpx数がマークアップされている画像](https://developer.paypay.ne.jp/static/img/expand_09.70d4aa9b.svg)

Text Label : 
[Label 16 Bold](../globalrule/typography.md)
Text Align-Left
#242323

Icon : 24px/dp

### Expand List

![Expandに余白などのpx数がマークアップされている画像](https://developer.paypay.ne.jp/static/img/expand_10.86c03d92.svg)

Text Label : 
[Body 14](../globalrule/typography.md)
Text Align-Left
#BABABA