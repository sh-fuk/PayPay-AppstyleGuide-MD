# Label

## Usage
* コンテンツの補足情報やステータスを明示するために利用します
*  画面内に複数のステータスラベルを利用する場合は、ステータスの差を明確に色分けして、視覚的に違いを認識できるようにします

### Usage Example
![複数あるステータスの表示](https://developer.paypay.ne.jp/static/img/label_01.fda538e4.svg)
![新しいコンテンツのPR](https://developer.paypay.ne.jp/static/img/label_02.cb20232c.svg)

## Type
![2枚のラベル部分の画像](https://developer.paypay.ne.jp/static/img/label_03.193cd04f.svg)

1 : 
Status Label
コンテンツ内で複数のステータスが存在する場合に、ステータスの違いを明示するために利用します。

![例](https://developer.paypay.ne.jp/static/img/label_04.28c91e82.svg)

ステータスを表す色はColor paletteの色の利用を推奨します。
特に「完了」や「エラー」を表す場合は、Functional Colorのカラーパレットを参照してください。

**Do/Don't**
タイトルは簡潔に、1行で収まるようにします。
![ラベル内にアクションアイテムを付与することは推奨しません / Don't](https://developer.paypay.ne.jp/static/img/label_05.19d28238.svg)
![ラベル内でテキストを改行することは禁止とします / Don't](https://developer.paypay.ne.jp/static/img/label_06.2e77c9a5.svg)

2 : 
New Label
新機能などユーザーにアピールしたい機能に利用します。
必要以上にユーザーの注意を惹きつけないよう、対象を1〜3回タップしたら消えるようにします。（回数は1回を推奨します）

**Don't**
[1画面内に複数のラベルを表示することは禁止します](https://developer.paypay.ne.jp/static/img/label_08.5397a467.svg)

## Spec
1. Status Label
![ステータスラベルの余白や感覚をマークアップした画像](https://developer.paypay.ne.jp/static/img/label_09.95ceffa1.svg)
Regular : 
[Heading / Label 12](../globalrule/typography.md)
Text Align-Center
#FFFFFF

Background color : 
[Use Color palette](../globalrule/color.md)

2. New Label
![newラベルの余白や感覚をマークアップした画像](https://developer.paypay.ne.jp/static/img/label_10.56976298.svg)
Regular : 
[Heading / Label 12](../globalrule/typography.md)
Text Align-Center
#FFFFFF

Background color : #FFB900