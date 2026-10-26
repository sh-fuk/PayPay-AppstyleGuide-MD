# Tab

## Usage
* 情報量の多い異なる情報群を一画面内に表示する際に利用します
* 1st viewで情報郡のサマリーを示し、タップすることで表示を切り替えられるようにします

### Usage Example
![Tabの使用例の画像](https://developer.paypay.ne.jp/static/img/tab_01.04cd37a3.svg)

## Type
![Tabの使用例2枚に番号が振られた画像](https://developer.paypay.ne.jp/static/img/tab_02.226ff149.svg)

1 : 
Regular
標準のタブナビゲーションです。タブの切り替えでタブ下のコンテンツ表示を切り替えます。


2 : 
Anchor link
画面内を移動するタブナビゲーションです。タブの切替で同一画面内のコンテンツ位置まで自動スクロールします。
スクロールとタブは連動しており、タブを切り替えなくても、画面内をスクロールしてコンテンツを表示すると、表示コンテンツのタブがアクティブの状態になります。

## Datail

### 1 Regular
![TabのRegular画像の中のコンポーネントに番号がマークアップされた画像](https://developer.paypay.ne.jp/static/img/tab_03.71281084.svg)

1 : 
Selected
タブが選択されている状態です。
画面が表示された際には左端のタブをデフォルトで選択されている状態を推奨します。
選択状態のタブに利用する色はPayPay Blueの利用を推奨しますが、サービスカラーに合わせて、色を変更することが可能です。
色を変更する場合、テキスト色は背景色と十分なコントラスト比を担保するようにしてください。

2 : 
Unselected
非選択状態のタブです。
タップで選択状態に切り替え、タブ下にコンテンツを表示します。

### 2 Anchor Link
![アンチャーリンクの画像の中のコンポーネントに番号がマークアップされた画像](https://developer.paypay.ne.jp/static/img/tab_04.27b908d9.svg)

1 : 
Selected
タブが選択されている状態です。
画面が表示された際には左端のタブをデフォルトで選択されている状態を推奨します。
選択状態のタブに利用する色はPayPay Blueの利用を推奨しますが、サービスカラーに合わせて、色を変更することが可能です。
色を変更する場合、テキスト色は背景色と十分なコントラスト比を担保するようにしてください。

2 : 
Unselected
非選択状態のタブです。
タップで選択状態に切り替え、同時にコンテンツエリアは同一画面内のコンテンツ位置まで自動スクロールします。

### ファーストビューに入りきらない場合
タブの数が多く、ファーストビューにタブをすべて表示することが難しい場合は、画面外へタブを表示することが可能です。
タブは水平方向にスワイプが可能です。
このUIを利用する場合、多くのユーザーはスワイプできることを認識できない場合があります。
画面外へタブが続くことが想起できるよう、右端のタブを見切れるように配置するなど配慮してください。
![入りきらない場合の例](https://developer.paypay.ne.jp/static/img/tab_05.1227cfb9.svg)

## Interaction
画面のスクロール時はタブは画面上部に固定し、スクロール操作中でもユーザーがいつでもタブのステータスの確認、切り替えができるようにします。

## Spec

### Regular
![Regularの具体的な間隔のマークアップ](https://developer.paypay.ne.jp/static/img/tab_07.227cc653.svg)

Label : 
**Active**
[Label 14 Bold](../globalrule/typography.md)
Text Align-Center
#3895FF
**Disabled**
[Label 14 Bold](../globalrule/typography.md)
Text Align-Center
#606060

Selected line : 2px / #3895FF

Background : #FFFFFF Shadow > [Low-shadow](../globalrule/shadow.md)

### Anchor Link
![Anchor Linkの具体的な感覚のpxのマークアップ](https://developer.paypay.ne.jp/static/img/tab_08.001d856c.svg)

Label : 
**Selected**
[Label 14 Bold](../globalrule/typography.md)
Text Align-Center
#FFFFFF
**Unselected**
[Label 14 Bold](../globalrule/typography.md)
Text Align-Center
#606060

Label background : 
**Selected**
#3895FF

Background : #F7F7F7