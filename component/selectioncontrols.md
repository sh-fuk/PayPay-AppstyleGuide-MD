# Selection Controls

## Usage
* アイテムの選択時に利用します
* アイテムは、役割や現在の状態を瞬時に認識できる表示でなくてはいけません
* アイテム単体では利用せず、必ず選択肢を示すテキストを併記します

### Usage Example
![](https://developer.paypay.ne.jp/static/img/selectioncontrols_01.3815d631.png)

## Type
![セクションコントロールの4種類の例画像](https://developer.paypay.ne.jp/static/img/selectioncontrols_02.b6c2475f.svg)

1 : 
Radio Button
単一選択の場合に利用します
ユーザーが選択できる項目は1つのみです
選択中のものではない項目が選択されると、それまで選択されていた項目は非選択の状態になります

![ラジオボタンの状態4種類の画像](https://developer.paypay.ne.jp/static/img/selectioncontrols_03.b88ce7ba.svg)

1. 非選択時 / Blank
2. 選択時 / Selected
3. 選択不可 / Disabled
4. 編集不可・選択時 / Disabled - Selected

2 : 
Checkbox
複数選択が可能な場合に利用します
Radio Buttonと異なり、ユーザーは同時に複数の項目を選択できます
選択された項目を再度選択すると非選択状態になります

![チェックボックスの状態4種類の画像](https://developer.paypay.ne.jp/static/img/selectioncontrols_04.64d12b6c.svg)

1. 非選択時 / Blank
2. 選択時 / Selected
3. 選択不可 / Disabled
4. 編集不可・選択時 / Disabled - Selected

3 : 
Select Button
単一選択・複数選択どちらの場合でも利用可能です
選択肢を横並びで利用したい場合、選択肢を目立たせたい場合に利用します
アプリ内での選択UIにはこのTypeの利用を推奨します

![セレクトボタンの状態2種類の画像](https://developer.paypay.ne.jp/static/img/selectioncontrols_05.9c67e992.svg)

1. 非選択時 / Blank
2. 選択時 / Selected

Select, Button内にはアイコンを含めることが可能です。
非選択時には色のついたアイコン、選択時には白色のアイコンを利用してください。

![画像付きセレクトボタンの例](https://developer.paypay.ne.jp/static/img/selectioncontrols_07.3a7e89c3.svg)

4 : 
Toggle Switch
項目に対してON/OFFを切り替える場合に利用します

![トグルスイッチのオンオフの画像](https://developer.paypay.ne.jp/static/img/selectioncontrols_06.924fae3b.svg)

1. 非選択時 / Blank
2. 選択時 / Selected

## Don't
![複数選択可能な項目にRadio Buttonを利用する / Don't](https://developer.paypay.ne.jp/static/img/selectioncontrols_08.3952560e.svg)
![単一選択の項目にCheck boxを利用する / Don't](https://developer.paypay.ne.jp/static/img/selectioncontrols_09.daaf0b77.svg)

## Spec
1 : Radio Button
    ![ラジオボタンのコンポーネントの間隔のpx数がマークアップされている](https://developer.paypay.ne.jp/static/img/selectioncontrols_10.8bf1aa4f.svg)
    Radio Button Icon : 
    24px*24px
    Inculding the padding inside of asset

    Radio Button Color : 
    **Blank**
    Stroke
    #BABABA
    1px
    Background
    #FFFFFF
    
    **Selected**
    Stroke
    #3895FF
    Background
    #FFFFFF
    Select
    #3895FF

    **Disabled**
    Stroke
    #DDDDDD
    1px
    Background
    #EEEEEE

    **Disabled-Selected**
    Stroke
    #DDDDDD
    1px
    Background
    #EEEEEE
    #BABABA

    Label : 
    [Label 16 Regular](../globalrule/typography.md)
    Text Align-Left
    #242323

2 : Checkbox
    ![チェックボックスのコンポーネントの間隔のpx数がマークアップされている](https://developer.paypay.ne.jp/static/img/selectioncontrols_11.5e35933f.svg)
    Checkbox Icon : 
    24px*24px/do
    Inculding the padding inside of asset

    Icon Color : 
    **Blank**
    Stroke
    #BABABA
    1px inside
    Background
    #FFFFFF

    **Selected**
    Background
    #3895FF
    Icon
    #FFFFFF

    **Disabled**
    Stroke
    #DDDDDD
    1px inside
    Background
    #EEEEEE

    **Disabled-Selected**
    Background
    #DDDDDD
    Icon
    #BABABA

    Label : 
    [Label 16 Regular](../globalrule/typography.md)
    Text Align-Left
    #242323

3 : Select Button
    ![セレクトのコンポーネントの間隔のpx数がマークアップされている](https://developer.paypay.ne.jp/static/img/selectioncontrols_12.b4cde27c.svg)
    Text Label : 
    **Selected**
    [Label 14 Bold](../globalrule/typography.md)
    Text Align-Center
    #FFFFFF

    Not Selected : 
    [Label 14 Bold](../globalrule/typography.md)
    Text Align-Center
    #909090

    Icon : 20px*20px/dp

    Background Height : 30px/dp

    background Color : 
    **Selected**
    Default: #3895FF
    Pressed(iOS): #3286E5

    **Not Selected**
    Default: #FFFFFF
    Pressed(iOS): #F2F2F2
    Stroke: #BABABA,1px/dp
    inside

    Background Corner : 
    Round = 15px/dp

4 : Toggle Switch
    ![オフ時のトグルスイッチのコンポーネントの間隔のpx数がマークアップされている](https://developer.paypay.ne.jp/static/img/selectioncontrols_14.74fff07d.svg)
    ![オン時のトグルスイッチの間隔のpx数マークアップ](https://developer.paypay.ne.jp/static/img/selectioncontrols_15.7ab98baa.svg)

    Button Size : H28*W48px/dp

    Icon Color : 
    **Selected**
    #3895FF

    **Unselected**
    #EEEEEE

    Button Shadow : 
    #000000
    Alpha 0.15
    X:0 Y:5
    Blur 6px

    Title : 
    [Label 16 Regular](../globalrule/typography.md)
    Text Align-Left
    #242323