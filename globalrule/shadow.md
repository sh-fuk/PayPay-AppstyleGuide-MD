# Shadow

## Principle
影は画面内の階層を明示するために使用します。
影は情報の優先度や必要なアクションを明確に示します。強調すべき箇所に効果的に使用することを推奨します。

## Usage

### 階層構造
画面内は複数の層の重なりで構成されます。より重要な情報を上位階層に表示します。階層構造を視覚的に明示することで、コンテンツの優先順位を明確にし、ユーザーは必要なアクションにたどり着きやすくなります。

各階層ごとに影を採用することで、表示階層を明確にします。画面内の光源/陰影は、方向、深さなどに一貫性を保ちます。

![階層構造のイメージ](https://developer.paypay.ne.jp/static/img/shadow_sect2_icons.2b358fb7.svg)

### 光源
光源は必ず上部90°方向にあるものとし、それ以外からの光源の設定は禁止とします。

![正しい光源（上部90°方向）](https://developer.paypay.ne.jp/static/img/shadow_sect2_no1.3b3204e7.svg)
![誤った光源（上部45°方向）](https://developer.paypay.ne.jp/static/img/shadow_sect2_no2.304fb1d5.svg)

### 陰影
配置される階層によって異なる陰影を設定します。
物理法則に基づき、階層が最背面より高ければ高いほど、影は淡く、大きくなります。

![1-6の影の濃さを示す画像](https://developer.paypay.ne.jp/static/img/shadow_sect2_images3.7ce93ff8.svg)

1 : Low-Shadow
2 : Middle-Shadow
3 : High-Shadow
4 : -90° Low-Shadow
5 : -90° Middle-Shadow
6 : -90° High-Shadow

## Type
![1-5段階で影の濃さを示す画像](https://developer.paypay.ne.jp/static/img/shadow_sect3_images.01b98638.svg)

1 : Low-Shadow
2 : Middle-Shadow
3 : High-Shadow
4 : White background
5 : Base

1. Low-Shadow
配置される階層によって異なる陰影を設定します。物理法則に基づき、階層が最背面より高ければ高いほど、影は淡く、大きくなります。

![](https://developer.paypay.ne.jp/static/img/shadow_sect3_cards1.62d1f37f.svg)

2. Middle-Shadow
Low-shadow階層にあるコンテンツより優先的に見せるべきコンテンツ、またはアクションコンポーネントを表示します。重なるコンテンツの下層が複雑なコンテンツ（地図や図柄など）である場合は、情報をより認識しやすくなるようこの階層に表示します。

![](https://developer.paypay.ne.jp/static/img/shadow_sect3_cards2.1563086a.svg)

3. High-Shadow
画面内で特に優先度の高い情報やアクションにのみ用います。画面内で多用することは禁止します。

![](https://developer.paypay.ne.jp/static/img/shadow_sect3_cards3.7d19d51b.svg)

### Don't
画面内で同階層に配置されているコンポーネントに別の深さのシャドウを指定することは禁止します。

![シャドウの値が揃っている](https://developer.paypay.ne.jp/static/img/shadow_sect3_no1.68c001c4.svg)
![シャドウの値が揃っていない](https://developer.paypay.ne.jp/static/img/shadow_sect3_no2.d9b3e337.svg)

4. White Background
コンテンツを表示する最も下の階層です。原則白色のみの利用を推奨します。

5. Base
この上には直接コンテンツを表示しません

## 視認性担保のためのシャドウ表現
写真や複雑なコンテンツの上にテキストやアイコンを配置する場合、配置するテキストやアイコンの視認性/可読性を十分に担保できるようにシャドウを用います。

![地図上にボタンを表示](https://developer.paypay.ne.jp/static/img/shadow_sect4_no1.3e3e87bb.svg)
![カメラ機能にアクションコンポーネントを表示](https://developer.paypay.ne.jp/static/img/shadow_sect4_no2.954ce466.svg)

## Spec

1 : Low Shadow : #000000 : Alpha 0.08 : X:0 Y:2 : Blur 6px
2 : Mid Shadow : #000000 : Alpha 0.15 : X:0 Y:6 : Blur 15px
3 : Mid Shadow : #000000 : Alpha 0.30 : X:0 Y:8 : Blur 20px
4 : Background : #FFFFFF
5 : Base Color : #F7F7F7
  : 視認性担保のためのシャドウ : 90° : #000000 Alpha 0.5 : #000000 Alpha 0