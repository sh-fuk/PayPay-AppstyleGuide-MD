# Slider

## Usage
* 選択可能な値の最小値と最大値の範囲から固定の値を選択、または範囲を選択できます
* 選択可能な範囲が可視化され、また選択時の状態も可視化されるため、相対的な値の認知が容易です
* キーボードでの値の入力やボタンのタップカウントよりも直感的な操作が可能です

### Usage Example
音量や価格の範囲の選択に利用します

![使用例のスクリーンショット3枚](https://developer.paypay.ne.jp/static/img/slider_sect2_images.855e1125.svg)

## Type

### Relative Slider
音量の調整など、特定の値を入力することが難しい場合に使用します。
バーの両端にアイコンを設置し、ユーザーはバー上の任意の位置を選択可能です。

![レリティブスライダーの例（音量スライダー）](https://developer.paypay.ne.jp/static/img/slider_sect3_images.f2db2dcd.svg)

### Range Slider
期間や料金の範囲の指定など、特定の2点の値の範囲を選択する場合に利用します。
両脇に値の最小値と最大値を表示し、ユーザーはバー上の2点の値を変更することで範囲の選択が可能です。

![レンジスライダーの例（金額選択）](https://developer.paypay.ne.jp/static/img/slider_sect4_images.ad5413d8.svg)

### Scale Slider
文字サイズの変更など、あらかじめ決められた値から選択する場合に利用します。
両端とバー上に選択可能なポイントを設定し、選択肢をテキストで表示します。ユーザーは設定されたポイントのみ選択可能です。
ポイントが設定されていない値は選択できません。

![スケールスライダーの例（文字サイズの設定）](https://developer.paypay.ne.jp/static/img/slider_sect5_images.ea19f6ac.svg)

## Detail

### Relative Slider

![レリティブスライダーの例のコンポーネントに番号がマークアップされている](https://developer.paypay.ne.jp/static/img/slider_sect6_images.0fa5563a.svg)

1 : 
Active Track
ユーザーの選択した範囲を表します
最小値から選択した値までをアクティブな色で表すことで、バー内での値を相対的に認識できます

2 : 
Active Point
バー上の未選択の値を表します

3 : 
Select Point
ドラッグでコントロール可能な部分です
アクションと同時に選択状態を表します

4 : 
Track Value
Sliderの役割りをアイコンで表現します
最小値と最大値の形状には差をつけ、役割りと状態を直感的に伝える必要があります

### Range Slider

![レンジスライダーの例のコンポーネントに番号がマークアップされている](https://developer.paypay.ne.jp/static/img/slider_sect7_images.fa736391.svg)

1 : 
Active Track
ユーザーの選択した範囲を表します。選択範囲をアクティブな色で表すことで、バー内での値を相対的に認識できます

2 : 
Inactive Track
バー上の未選択の値を表します

3 : 
Active Point
ドラッグでコントロール可能な部分です。アクションと同時に選択状態を表します

4 : 
Track Value
左端に最小値、右端に最大値をテキストで表示します

5 : 
Input Value Balloon (Option)
選択範囲中の最小値、最大値をテキストで表示します。表示は任意ですが、表示することでユーザーの利便性は向上します。挙動についてはInterctionの項目を参照してください

### Scale Slider
![スケールスライダーの例のコンポーネントに番号がマークアップされている](https://developer.paypay.ne.jp/static/img/slider_sect8_images.f6dcb3b7.svg)

1 : 
Sample Value (Option)
値の示す状態を表示します。表示は任意ですが、表示することでユーザーは選択可能な値をより直感的に知ることができます。選択された値のSample Valueもアクティブ状態になります

2 : 
Inactive Point
未選択のPointです。Scale Sliderの場合、Inactive Point以外は選択できません。バーをタップした場合、タップ位置がより近いInactive Pointが選択されます

3 : 
Active Point
値が選択された状態です

4 : 
選択可能な値をテキストで表示します。簡潔に短文で表示します。2〜4文字以内のテキスト数を推奨します

## Interaction

### Select Feedback
アニメーションを利用して、状態の変化をより明確に伝えます。
また、選択が完了したことをより直感に伝えるために、iOSではHaptic Feedbackを利用することを推奨します

Active Pointは選択された値のPointまでスライドして移動します
![選択時のActive Pointの移動](https://developer.paypay.ne.jp/static/img/slider_sect9_images1.26291156.svg)

操作中のActive PointのInput Value Balloonは拡大されます
拡大することで、操作中の値をより明示的にします
指を離し値が確定するとBalloonは元の大きさに戻ります
![選択時のInput Value Balloonの拡大](https://developer.paypay.ne.jp/static/img/slider_sect9_images2.ad0379cb.svg)

### Support Feedback
ユーザーの選択した状態を明確に示すために、選択時にフィードバックを追加することを推奨します。
以下はフィードバックの例です。

選択した値のテスト音を鳴らし、選択した音量を確認することができます
![音量設定](https://developer.paypay.ne.jp/static/img/slider_sect10_images1.96ffc753.svg)

スライダーの下部にサンプルUIを表示し、スライダーの選択した値と連動してUI上のテキストサイズの大きさを変化させ、実際のサイズを確認することができます
![文字サイズ設定](https://developer.paypay.ne.jp/static/img/slider_sect10_images2.4575e674.svg)

![価格の選択](https://developer.paypay.ne.jp/static/img/slider_sect10_images3.fe29357f.svg)

## Specs

### Relative Slider
![レリティブスライダーの具体的なpx数のマークアップ画像](https://developer.paypay.ne.jp/static/img/slider_sect11_images.9e09e0e1.svg)

Active Track : 
Hight : 2px/dp
Corner Round : 2px
#3895FF

Inactive Track : 
Hight : 2px/dp
Corner Round : 2px
#EEEEEE

Active Point : 
12*12px/dp
タップエリアは35*35px/dp以上担保します

Track Value : 
24*24px/dp

### Scale Slider
![スケールスライダーの具体的なpx数のマークアップ画像](https://developer.paypay.ne.jp/static/img/slider_sect12_images1.f91912e3.svg)
![スケールスライダーの数値吹き出しの具体的なpx数のマークアップ画像](https://developer.paypay.ne.jp/static/img/slider_sect12_images2.943b2bdb.svg)

Active Track : 
Hight : 2px/dp
Corner Round : 2px
#3895FF

Inactive Track : 
Hight : 2px/dp
Corner Round : 2px
#EEEEEE

Active Point : 
12*12px/dp
タップエリアは35*35px/dp以上担保します

Track Value (Text) : 
[Label 14 Regular](../globalrule/typography.md)
Text Align-Center
#242323

Input Value Balloon (Option) : 
**Back ground**
#FFFFFF
Shadow: [Low Shadow](../globalrule/shadow.md)

**Normal 数字**
[Label 16 Body](../globalrule/typography.md)
Text Align-Center
#3895FF

**Normal 単位（漢字表記）**
[Label 12](../globalrule/typography.md)
Text Align-Center
#3895FF

**Selected 数字**
[Label 20 Bold](../globalrule/typography.md)
Text Align-Center
#3895FF

**単位（漢字表記）**
[Label 14 bold](../globalrule/typography.md)
Text Align-Center
#3895FF

### Scale Slider
![スケールスライダーの具体的なpx数のマークアップ画像](https://developer.paypay.ne.jp/static/img/slider_sect13_images.3f7da23d.svg)

Sample Value (Option) : 
**Default**
[Label 14 Regular](../globalrule/typography.md)
Text Align-Center
#606060

**Selected**
[Label 14 Bold](../globalrule/typography.md)
Text Align-Center
#3895FF
テキストサイズは用途によって変更可能です

Inactive Line : 
Hight : 2px/dp
Corner Round : 2px
#EEEEEE

Inactive Point : 
**Default**
12*12px/dp
タップエリアは35*35px/dp以上担保します
**Selected**
20*20px/dp
タップエリアは35*35px/dp以上担保します

Track Value : 
**Default**
[Label 12 Regular](../globalrule/typography.md)
Text Align-Center
#909090