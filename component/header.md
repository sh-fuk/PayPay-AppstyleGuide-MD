# Header

## Usage
* 画面のタイトルやアクションアイテム、ナビゲーションアイテムを表示します
* 画面上に表示されるコンテンツの内容やこれから行うアクションの目的を簡潔にわかりやすく表示します
* 表示されている画面の階層を明らかにし、簡単に上位階層の画面へ移動できるようにします
* HeaderはOSの表示仕様に準拠します

### Usage Example
![iOS](https://developer.paypay.ne.jp/static/img/header_sect2_images1.510d0483.svg)
![Android](https://developer.paypay.ne.jp/static/img/header_sect2_images2.89d570ca.svg)

## Type
![iPhone2種類、Android2種類のヘッダーの画像](https://developer.paypay.ne.jp/static/img/header_sect3_images.a1d1b5d4.svg)

1. : 
Regular
白い背景のHeaderです。
設定画面など、コンテンツ要素が少なくユーザーアクションを簡潔に完了させたい画面に利用します。

2. : 
Transparent
透過背景のHeaderです。
コンテンツエリアはHeaderエリアまで拡張ができ、Headerの背景に任意の色を設定できます。
メイン機能など、コンテンツエリアを広く見せたい場合などに利用します。

## Transparent
主要コンテンツやキャンペーンなど、コンテンツエリアを広く強調して見せたい場合は、下図のようにヘッダーエリアの背景色の領域を拡張します。
背景色はグラデーションカラーを推奨します。
![例](https://developer.paypay.ne.jp/static/img/header_sect4_images.4a16289c.png)

## Detail
![iOS](https://developer.paypay.ne.jp/static/img/header_sect5_images1.ba3b1825.svg)
![Android](https://developer.paypay.ne.jp/static/img/header_sect5_images2.05fff674.svg)

1. : 
Navigation Item
ナビゲーションアイテムは画面間の移動に使用します。
表示されている画面の階層を明らかにし、簡単に上位階層の画面へ移動できるようにします。

Drill downで表示された画面に表示 / タップで上位階層の画面に戻る
![Back button](https://developer.paypay.ne.jp/static/img/header_sect6_images1.57007f48.svg)

Slide UPで表示された画面に表示 / タップで画面を閉じる
![Close button](https://developer.paypay.ne.jp/static/img/header_sect6_images2.d01eb2c9.svg)

2. :
Title
タイトルには以下の内容を記載します。
* 画面名
* 機能名
* アクション名
タイトルは端末のOS仕様に準拠し、端末の幅によって表示テキスト数は異なります。簡潔でコンパクトなタイトルの表示を推奨します

**Do/ Don't**
タイトルは簡潔に、1行で収まるようにします。

[The title is contained in one line. / Do](https://developer.paypay.ne.jp/static/img/header_sect8_images1.bc85e85b.svg)
[The title is truncated. / Don't](https://developer.paypay.ne.jp/static/img/header_sect8_images2.81b82329.svg)

3 : Action Items/(Optional)
**アイコン**
アクションアイコンを最大2つまで表示できます。表示するアイコンは画面内の機能に関連性のある機能である必要があります。

![アクションのアイコンの例画像](https://developer.paypay.ne.jp/static/img/header_sect9_1subimage2.0afb8858.svg)

**テキストボタン**
テキストボタンを表示できます。
表示するアイコンは画面内の機能に関連性のあるものである必要があります。
基本的にはアイコンボタンの利用を推奨します。
テキストボタンは、アイコンのみでは表現することが難しい場合、より強調するべき機能の場合に使用します。

テキストボタンとタイトルテキストの間には十分な余白を設け、テキストの視認性/可読性を担保してください。
ボタンのラベルテキストは簡潔で短いテキストを使用します。2文字程度を推奨します。
![保存](https://developer.paypay.ne.jp/static/img/header_sect9_2subimage1.18929d65.svg)

編集コンテンツの保存ボタン
編集画面では、編集内容を保存する際に「保存」ボタンを表示します。
保存ボタンは編集状態によって表示を切り替えます

![有効化された保存ボタンと無効化された保存ボタンの2枚の画像](https://developer.paypay.ne.jp/static/img/header_sect9_2subimage.0e3e58cc.svg)

1 : Active : 変更された情報がある場合は「保存」ボタンを活性化し、ユーザーアクションを促します。
2 : Disable : 編集内容に変更がない場合は「保存」ボタンは非活性にします。

## Interaction

### Scroll
画面スクロール時は、ヘッダーは画面上部に固定表示されます。

![固定されたヘッダー](https://developer.paypay.ne.jp/static/img/header_sect10_images1.6ed74ee3.svg)

1st viewで表示される重要なコンテンツをスクロール時にも表示したい場合は、ヘッダーに表示することができます。

![残高が表示されたヘッダーが上部に固定されている](https://developer.paypay.ne.jp/static/img/header_sect10_images2.ba62cc69.svg)

## Spec
![iOSのヘッダーに余白や間隔のpxがマークアップされている](https://developer.paypay.ne.jp/static/img/header_sect11_images1.196d02b0.svg)
![Androidのヘッダーに余白や間隔のpxがマークアップされている](https://developer.paypay.ne.jp/static/img/header_sect11_images2.9ac2a416.svg)

### Items
Navigation Item : 24px*24px/dp

Title : 
**Regular**
[Heading16](../globalrule/typography.md)
Text Align-Center
#242323

**Transparent**
[Heading16](../globalrule/typography.md)
Text Align-Center
#FFFFFF / #242323
Title text colorはBackground colorとのコントラスト比を十分に担保してください。
テキストカラーはヘッダーの背景色に応じて上記2色のどちらかを使用してください。

Action Item : 
24*24px/dp
**Text- Active**
[Label 14 Bold](../globalrule/typography.md)
Text Align-Center
#3895FF

**Text- non Active**
[Label 14 Bold](../globalrule/typography.md)
Text Align-Center
#BABABA

Background : 
**Regular**
#FFFFFF
**Transparent**
--