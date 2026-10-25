# Card

## Principle
* 複雑な情報を整理しグルーピングして提示する際に使用します
* カードそのものがタップやスワイプアクションをアフォードします
* 情報整理やアクションをアフォードする以外の用途、装飾のためだけにカードUIを使用することはしません

## Usage

### Usage Example
![複雑な情報をグルーピング](https://developer.paypay.ne.jp/static/img/card_sect2_images1.4c5b2e95.svg)

## Detail
![カード上に1-2がマークアップされている](https://developer.paypay.ne.jp/static/img/card_sect3_images1.ea15b932.svg)

1 : Contents Area : Card内にコンテンツを表示する場合は、コンテンツの周囲に十分な余白を設け、可読性を担保します。カードはタップ、スワイプするインタラクションをアフォードしますが、よりアクションを明示的にするためにテキストリンクやアイコンの表示を推奨します。
2 : Background : [Shadow](../globalrule/shadow.md)の項目の階層構造、光源、陰影のガイドラインに準拠し、カードの背景にシャドウを表示します。

## Do / Don't
![コンテンツがコンテンツエリア外に表示されている](https://developer.paypay.ne.jp/static/img/card_sect4_no1.99566e6d.svg)
![同階層上のカードに異なるシャドウを使用する](https://developer.paypay.ne.jp/static/img/card_sect4_no2.0c9a3a3c.svg)
![シャドウに色をつける](https://developer.paypay.ne.jp/static/img/card_sect4_no3.2b7e2989.svg)
![カードがページのグリッドに沿っていない](https://developer.paypay.ne.jp/static/img/card_sect4_no4.6a594c44.svg)

## Interaction
Tap : 
アクション時にタップフィードバックを表示します。
Specを参照してください。
参考：[Interaction](../globalrule/interaction.md)

Flip : 
横に並ぶカードをFlipで移動させるインタラクションを使用する場合、タップフィードバックは表示しません。

## Spec

![カードに余白等のpx数がマークアップされている画像](https://developer.paypay.ne.jp/static/img/card_sect6_images1.ccd775ae.svg)

カード周辺、カード間の余白の値については、[Layout](../globalrule/layout.md)の項目を参照してください。

Background : 
Default > #FFFFFF,
Pressed( iOS ) > #F2F2F2
Corner : 40px/dp
Shadow : 40px/dp
