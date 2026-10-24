# Color

## Principle
色は情報の優先度や必要なアクションを明確に示します。特定の色を固有のアクションやステータスにあてはめることで、サービス全体で一貫性を保ち、ユーザーの学習コストを軽減します。
提供するUIは必ずコンポーネントに定義された色を使用します。使用する色を統一することで、ブランドの個性を醸成します。
全てのコンテンツは可読性、視認性を十分担保し、あらゆる人が快適に閲覧できる配色を利用しなくてはいけません。

## Color Definition Pattern
PayPayの色はBrand color、Global color、Extended colorの3種類に定義されます。

## Brand Color
Brand colorはPayPayのブランドそのものを表すカラーであり、ロゴに利用されるカラーです。
PayPayロゴ以外の要素に利用することは推奨しません。
![](https://developer.paypay.ne.jp/static/img/BrandColor.91df13dd.svg)

## Global Color Assets
Global color assetsは、PayPayそのものを表すカラーアセットです。
Brand colorを中心とした4色の組み合わせ、または定義されたグラデーションで展開します。

この色の組み合わせを利用することでユーザーはPayPayのブランドを認知します。

PayPayブランド全体を表現する場合は単色4色の組み合わせを、Consumer Appを表現する場合はグラデーションカラーの利用を推奨します。
![](https://developer.paypay.ne.jp/static/img/global_color_asset.077754c7.svg)

### Color Palette
PayPay Red : #FF0033
Blue : #3895FF
Navy : #002970
White : #FFFFFF

### Gradation Palette
PayPay Gradation : 
#FF0033
↓
#FF3B62

### Usage Example
![Brand Logo](https://developer.paypay.ne.jp/static/img/brand_logo.7f26c7d9.svg)
![UI Parts](https://developer.paypay.ne.jp/static/img/ui_parts.77b46810.svg)
![System Icon](https://developer.paypay.ne.jp/static/img/system_icon.dedfed6c.svg)
![UI Background](https://developer.paypay.ne.jp/static/img/ui_background.906ad7ab.svg)

### Don't
![example image](https://developer.paypay.ne.jp/static/img/global_dont.c505ac7a.svg)
Global Colorの配色でハレーションをおこすなどの
ユーザーに不快感を与えるような使い方は禁止します

## Extended Color Assets
Extended color assetsは、Global colorを含むカラーアセットです。
UIコンポーネントや、イラストやアイコンなど、コンテンツにアクセントが必要な際に利用します。

PayPayのデザインフィロソフィーである"Empathy" "Happy"を表現する、楽しく、親しみやすく、安心感のある配色で展開します。

### Color Palette
有彩色12色相を4階調、無彩色を8階調で展開します。
UIへの利用は01行、04行の利用を推奨します。
UIに04行の色を利用する場合は、コンテンツの背景色への利用を推奨します。
04行の色をテキストやアクションパーツに利用することは禁止します。

イラスト表現などでパレットにない階調の色の利用が必要な場合は、任意の色を利用することを許容します。

#### 有彩色
01 : #FF0033 -- #FA1919 -- #FC6600 -- #FFB900 -- #56D32A -- #26BF7D
02 :           -- #FD5C5C -- #FF954C -- #FFC733 -- #79D957 -- #52CC97
03 :           -- #FFB2B2 -- #FFBA8B -- #FFE39A -- #BCF1A9 -- #A1E5C8
04 :           -- #FFE5E5 -- #FFF0E5 -- #FFF7E5 -- #E5F7DF -- #DFF7ED
---
01 : #00C2C2 -- #00B9F5 -- #3895FF -- #002970 -- #7921A3 -- #F23099
02 : #41D9D9 -- #33CDFF -- #4DA0FF -- #2455AA -- #9047B2 -- #FF4CAD
03 : #8AE7E7 -- #BAEEFF -- #BADAFF -- #BBCFF2 -- #D9B0EC -- #FFB4DD
04 : #DFF7F7 -- #E5F8FF -- #E5F1FF -- #DDEAFE -- #F7E5FF -- #FFE5F3

#### 無彩色
01 : #242323
02 : #606060
03 : #909090
04 : #BABABA
05 : #DDDDDD
06 : #EEEEEE
07 : #F7F7F7
08 : #FFFFFF

### Usage Example
![Illustration](https://developer.paypay.ne.jp/static/img/ext_color_usage_example_1.766664af.svg)
![UI Parts](https://developer.paypay.ne.jp/static/img/ext_color_usage_example_2.17bd2a7c.svg)

## Functional Color
Functional color assetsは役割を持つ色のアセットです。
色の持つ役割に一貫性を保つことで、ユーザーの学習コストを軽減させ、快適なUXを提供します。
色はExtended color assetsから引用します。

### Color Palette
Success : #20BF7A
Error/Alert : #FD5C5C
Caution/Pending : #FFB900
Action/Information : #3895FF

### Usage Example
![Success](https://developer.paypay.ne.jp/static/img/usage_success.d60d408b.svg)
![Error](https://developer.paypay.ne.jp/static/img/usage_error.4caf6cfc.svg)
![Pending](https://developer.paypay.ne.jp/static/img/usage_pending.99cf1080.svg)
![Information](https://developer.paypay.ne.jp/static/img/usage_info.e2dddec8.svg)

### Don't
以下の使い方はユーザーの誤操作を誘発するリスクがあるため禁止とします。

![Function colorを定義された色以外で利用する](https://developer.paypay.ne.jp/static/img/dont1.ef45106e.svg)
![アクションコンポーネント以外にアクションカラーを多用する](https://developer.paypay.ne.jp/static/img/dont2.b954af64.svg)

## Gradation Color
連携サービスのUIを構成するカラーやマーケティングツールには、Extended color assetsを元に構成したグラデーションカラーの利用が可能です。
ただし、Global colorで定義されているPayPay GradationをPayPayのメイン機能以外で利用することは禁止します。

グラデーションカラーを利用する場合は、定義されたルールに則ってください。

### Gradation Color Rule
![下の表の1や2の記号が記入された図](https://developer.paypay.ne.jp/static/img/Gradation_Rule.3a6bd7fd.svg)
| 方向 | グラデーションの方向は90度方向のみとします。色の指定位置は (1) 0%地点と (2) 100%地点のみとします。(1) と (2) に異なる色相の色を指定することは問題ありません。異なる色相を指定する場合は、色相の近いものを指定してください。色相が離れすぎている色の選択は禁止とします。 |
| 1 Top | グラデーションの上部（0%位置）には明度の高い色を指定します。Color Paletteで定義する色相の利用を推奨します。明度は90-100の間を推奨します。 |
| 2 Bottom | グラデーションの下部（100%位置）には　(1)　より明度、彩度の低い色を指定します。明度は80-100の間を推奨します。 |

### Usage Example
![UI Background](https://developer.paypay.ne.jp/static/img/Illustration_US4.85555b66.png)
![Illustration Background](https://developer.paypay.ne.jp/static/img/UI_Background_US4.c009507c.svg)

### Don't
![グラデーションに3色以上を指定する](https://developer.paypay.ne.jp/static/img/usage_dont_01.2419824f.svg)
![上部に濃い色、下部に明るい色を指定する](https://developer.paypay.ne.jp/static/img/usage_dont_02.9c6b50a7.svg)
![指定する色の明度が80以下](https://developer.paypay.ne.jp/static/img/usage_dont_03.53de3a21.svg)
![色を透過する](https://developer.paypay.ne.jp/static/img/usage_dont_04.b75cedbf.svg)
![色相の遠い色を組み合わせる](https://developer.paypay.ne.jp/static/img/usage_dont_05.da639f08.svg)
![連携サービスやミニアプリなど、PayPayの主要機能以外にPayPay Gradationを利用することは禁止します](https://developer.paypay.ne.jp/static/img/usage_dont_06.544048b2.png)

## Accessibility
主要なコンテンツに文字を表示するには、背景色と前景色はコントラスト比3:1以上を担保します。
ただし、付随的なコンポーネント、テキストが装飾要素である場合は除きます。
また、ロゴまたはブランド名の一部である文字には最低限のコントラストの要件はありません。