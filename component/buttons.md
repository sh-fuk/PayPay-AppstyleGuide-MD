# Buttons

## Usage
* タップすることでアクションを実行することができます
* アクション可能であることや内包するアクション、ステータスを明示し、タップ後のインタラクションが想定できるようにします
* ボタンは画面内の他のコンテンツと視覚的に差別化し、目立つように配置する必要があります

### Usage Example
![入力要素の送信](https://developer.paypay.ne.jp/static/img/buttons_01.043b955d.svg)
![選択肢の送信](https://developer.paypay.ne.jp/static/img/buttons_02.d85728b9.svg)

## Type
状態によりいくつかの種類があり、用途によって使い分けをします

### Action Button

![6つのボタン状態の画像](https://developer.paypay.ne.jp/static/img/buttons_03.ef6efa2a.svg)

1 : Action button Primary : 高優先度のアクションに利用します
2 : Action button Secondary : 中優先度のアクションに利用します
3 : Action button Tertiary : 低優先度のアクションに利用します
4 : Action button Alert : ユーザーデータの削除など、誤ったアクションによりユーザーが不利益を被るであろうアクションに利用します
5 : Action button Disabled : アクションが無効の状態に利用します

## Layout

### 画面内のボタンの優先順位
画面内に複数のボタンを配置する場合、ボタンの優先順位を設定し、優先順位に沿ったTypeのボタンを配置します。
ユーザーがアクションの選択に迷ってしまわないように、優先順位は明確である必要があります。

![実際のPayPayで使われてる画面と上のボタン種類の対応マークアップ](https://developer.paypay.ne.jp/static/img/buttons_04.8e99450a.png)

### Do/ Don't
画面内のボタンの優先順位が不明瞭になるような使い方は禁止とします。

![選択肢の優先順位が明確](https://developer.paypay.ne.jp/static/img/buttons_05.a842b0e8.svg)
![選択肢の優先順位が不明瞭](https://developer.paypay.ne.jp/static/img/buttons_06.537a30a4.svg)

### Horizontal Button
優先順位や機能が同等の情報を表示する場合は、アクションボタンを横並びに最大2つまで配置することを許容とします。
3つ以上の選択肢を設ける場合は、ボタンを縦に並べる、または他のUIにしてください。

ボタンの背景色は、2つのボタンが異なるアクションであると容易に認識できるよう、色差のある2色の利用を推奨します。
色は[Color palette](../globalrule/color.md)の色を参考にしてください。

![](https://developer.paypay.ne.jp/static/img/buttons_07.051f6d69.svg)

### 2つのボタンの背景色について
色は[Color palette](../globalrule/color.md)の色を参考に指定してください

異なる2色を指定する場合 : 2つのボタンが異なるアクションであると容易に認識できるよう、色差のある2色の利用を推奨します。画面上で調和の取れた2色を選択してください。PayPayのPrimary Buleの利用は必須ではありません
同色の場合 : 2つのボタンが異なるアクションであると容易に認識できるよう、アイコンを表示することを推奨します

### Sticky Button
コンテンツ量が多く、縦に長い画面の最下部にアクションボタンを配置する場合、1st viewでボタンを認識できるように、画面下部にボタンを固定するSticky Buttonの使用を推奨します。

表示コンテンツの上位階層にボタンを配置し、ボタンの周辺には十分な余白を担保します。
Sticky Buttonの表示エリア外の領域をスクロール領域とします。

![](https://developer.paypay.ne.jp/static/img/buttons_08.a54d687f.svg)

### Keyboard Button
ユーザーが入力アクションをする画面では、ボタンをキーボード上部に固定表示します。
ボタンの上下左右には十分な余白を設け、隣接するコンテンツやキーボードとの誤タップを避けます。

![](https://developer.paypay.ne.jp/static/img/buttons_09.5d1a349b.svg)

## Detail

### Action Button

![1〜3の番号がボタンにマークアップされた画像](https://developer.paypay.ne.jp/static/img/buttons_10.1b85782c.svg)

1 : Text Label
2 : Background
3 : Icon

1. Text Label
テキストラベルには、ユーザーアクションをすぐに理解できる簡潔なテキストを使用します。
アクションを明確に伝えるために、動詞での表示を推奨します。
（Pay / 支払う など）

## Do/ Don't
簡潔で短く、すぐにアクションが理解できるテキストを設定してください。
ボタンのテキストが途中で切れてしまうこと、2行になることは禁止します。

![アクションが明快で短く、テキストが1行に収まる / Do](https://developer.paypay.ne.jp/static/img/buttons_12.a842b0e8.svg)
![テキストが長くアクションが不明瞭・途中で切れる、2行になる / Don't](https://developer.paypay.ne.jp/static/img/buttons_13.537a30a4.svg)

2. Background
ボタンの役割や優先順位をアプリ内で統一し、ユーザーの学習コストを軽減するため、ボタンの色は定義された色以外を使用しません。
例外として、黒などの濃い背景色または写真の上に配置する場合のみ、白枠・白テキストのボタンの使用を許容します。

![黒色背景時のボタン例・写真上のボタン例](https://developer.paypay.ne.jp/static/img/buttons_14.812306f5.png)

3. Icon
ボタンが示す内容をより視覚的に伝えたい場合はアイコンをラベル内に含めます。
アイコンは字色と同色の使用を推奨します。
例外として、白い背景のボタンの場合は、文字色と異なる色のアイコンの利用を許容とします。
任意の色をアイコンに使用する場合は、背景色とアイコンの色の色差、コントラスト比を十分に担保してください。

![ボタン2種類](https://developer.paypay.ne.jp/static/img/buttons_0123.79c04666.svg)

## Do/ Don't
![アイコンの視認性が担保されている / Do](https://developer.paypay.ne.jp/static/img/buttons_15.8246def3.svg)
![アイコンの視認性が悪い / Don't](https://developer.paypay.ne.jp/static/img/buttons_16.1598bd37.svg)
![アイコンのみの表示](https://developer.paypay.ne.jp/static/img/buttons_18.e45e841b.svg)
![アイコンをつけることで情報の優先順位が不明瞭になる](https://developer.paypay.ne.jp/static/img/buttons_17.f1bf7bd6.svg)
![ボタンステータスとアイコンの表す意味が合っていない](https://developer.paypay.ne.jp/static/img/buttons_19.b707e293.svg)

## Interaction
アクション時にタップフィードバックを表示します。
Specを参照してください。

参照：[Interaction](../globalrule/interaction.md)

## Spec

### Action Button

![ボタン2種類にpx数がマークアップされた画像](https://developer.paypay.ne.jp/static/img/buttons_20.949cf4ac.svg)

| 種類 | 詳細 |
| :--- | :--- |
| Text label | **Primary, Error, Disabled**<br>[Heading / Label 14](../globalrule/typography.md)<br>Text Align-Center<br>Default:#FFFFFF<br>Pressed(IOS):#FFFFFF,Alpha 0.7 |
| Text label | **Secondary, Tertiary**<br>[Heading / Label 14](../globalrule/typography.md)<br>Text Align-Center<br>Default:#3895FF<br>Pressed(IOS):#3895FF,Alpha 0.7 |
| Background | **Primary**<br>Default:#3895FF<br>Pressed(IOS):#3286FF |
| Background | **Error**<br>Default:#FD5C5C<br>Pressed(IOS):#E35353 |
| Background | **Disabled**<br>#EEEEEE |
| Background | **Secondary**<br>Default<br>Background:#FFFFFF<br>Stroke:#389FF,1px/dp,inside<br><br>Pressed(iOS)<br>Background:#F2F2F2<br>Stroke:#3286E5,1px/dp,inside |
| Background | **Tertiary**<br>Default:#FFFFFF<br>Pressed(iOS):#F2F2F2 |
| Background Corner | Round = 8px/dp |
| Icon Size | 20 * 20px/dp<br>Pressed(iOS):Alpha 0.7 |

### Spacing
![](https://developer.paypay.ne.jp/static/img/buttons_21.e200746f.svg)
![](https://developer.paypay.ne.jp/static/img/buttons_22.fb022d2d.svg)

### Sticky Button
![Button 1つ](https://developer.paypay.ne.jp/static/img/buttons_23.d13ea826.svg)
![Button 2つ以上](https://developer.paypay.ne.jp/static/img/buttons_24.e2ea3a9a.svg)

Background Color : #FFFFFF
Shadow : 背景上部にShadowを付与 : Shadow : [-90° Low-Shadow](../globalrule/shadow.md)

### Keyboard Button

![](https://developer.paypay.ne.jp/static/img/buttons_25.ff3e4d8b.svg)