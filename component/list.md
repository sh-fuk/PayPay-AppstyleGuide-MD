# List

## Usage
* 複数ある情報を整理し、一覧性を高く表示する際に利用します
* 現在のステータスやアクション内容がある場合は簡潔に示します
* リスト内の構成には規則性を設け、瞬時に内容を把握・比較できるように情報の整理をします
* テキストやアイコンで何を示しているか簡潔に伝え、その詳細やアクション内容も同じく簡潔に表示します
* リストの体裁はOS標準のUIに準拠します

### Usage Example
![例](https://developer.paypay.ne.jp/static/img/list_sect2_images.28bbd72d.svg)

## Type
Regular List / Single line
![iOS](https://developer.paypay.ne.jp/static/img/pagecontrols_sect3_images1.18a671ef.svg)
![Android](https://developer.paypay.ne.jp/static/img/pagecontrols_sect3_images2.99858d06.svg)

Regular List / Multi-line
![iOS](https://developer.paypay.ne.jp/static/img/pagecontrols_sect3_images3.16519f8b.svg)
![Android](https://developer.paypay.ne.jp/static/img/pagecontrols_sect3_images4.208408ac.svg)

Action Component List
![iOS](https://developer.paypay.ne.jp/static/img/pagecontrols_sect3_images5.e3817860.svg)
![Android](https://developer.paypay.ne.jp/static/img/pagecontrols_sect3_images6.bc3acbb0.svg)

Edit List
![iOS](https://developer.paypay.ne.jp/static/img/pagecontrols_sect3_images7.f8688d34.svg)
![Android](https://developer.paypay.ne.jp/static/img/pagecontrols_sect3_images8.4c13ed86.svg)

Alternative List
![iOS](https://developer.paypay.ne.jp/static/img/pagecontrols_sect3_images9.7d860fb1.svg)
![Android](https://developer.paypay.ne.jp/static/img/pagecontrols_sect3_images10.0312a236.svg)

## Detail

### Regular List
![listに1-6のマークアップされている画像](https://developer.paypay.ne.jp/static/img/list_sect4_images.c6aaf942.svg)

1 : 
List Header
複数のリストをグルーピングし、大項目としてタイトルを付与する場合に利用します

2 :
List Sub Header (Option)
1のリストヘッダーの中でさらに小項目に分類しタイトルを付与する場合に利用します大項目は必ず1リストヘッダーとし、2サブリストヘッダーを大項目として利用することはできません

3 : 
Icon (Option)
テキストの内容を視覚的に示す場合、アイコンを配置します

4 : 
Title
コンテンツを簡潔に短文で表示します1行以内に収まる文字数を推奨します

5 : 
Description (Option)
Titleを説明する補足的なテキストを表示します4Titleと同様に簡潔に短文で表示します1行以内に収まる文字数を推奨します

6 : 
Action Item (Option)
コンテンツのステータスや、アクション可能なアイテムを右寄せで配置しますテキストを表示する場合は5文字以内を推奨しますTitleやDescriptionとの間に十分な余白を担保しますiOS/Webの場合、タップして下層画面に遷移可能なリストには必ずアイコンを付与しますAndroidにはアイコンを付与しません

### Action Component List
![](https://developer.paypay.ne.jp/static/img/list_sect5_images.31ffb603.svg)

1 : ボタンを配置
2 : トグルスイッチを配置

### Edit List
![Edit List](https://developer.paypay.ne.jp/static/img/list_sect6_images.fedf7c0c.svg)

1 : 未入力
2 : 入力中
3 : 入力済み・非選択時
4 : エラー

## Interaction

### Tap
Expand areaをタップして、展開前/展開後のUIを切り替えます。
タップ時にはタップフィードバックを表示します。
Specを参照してください。

参考：[Interaction](../globalrule/interaction.md)

### Scroll
List Headerのあるリストの場合、スクロール時に画面のHeader直下にList Headerを固定します。
List Headerを固定することでスクロール中に表示されているリストの情報を明確に伝えることができます。

![](https://developer.paypay.ne.jp/static/img/list_sect8_images.d72c94f1.svg)

## Specs

### Cross-platform adaptation
OSごとにListの各パーツの表示に差異があります。

![List](https://developer.paypay.ne.jp/static/img/list_sect9_images.943b6583.svg)

|  | iOS | Android |
| :--- | :--- | :--- |
| 1 Action Item | タップして下層画面に遷移可能なリストには必ずアイコンを付与します | 遷移できる・できないにかかわらずアイコンを置かない |
| 2 Divider | 罫線の左端に16pxのMarginを付与 | 罫線の端にMarginを付与しない |


List Header : 
![](https://developer.paypay.ne.jp/static/img/list_sect10_images.09c79aec.svg)
    Font : 
    [Heading 16](../globalrule/typography.md)
    Text Align-Left
    #606060

    Background : 
    #FFFFFF

    Scroll : 
    Shadow > [Low-shadow](../globalrule/shadow.md)

List Sub Header (Option) : 
![サブヘッダーの余白や間隔](https://developer.paypay.ne.jp/static/img/list_sect11_images.3dab681c.svg)
    Font : 
    Heading 14
    Text Align-Left
    #909090
    Background : 
    #FFFFFF

Icon : 
![Icon](https://developer.paypay.ne.jp/static/img/list_sect12_images.732a1c06.svg)
    List Icon : 
    24*24px/dp
    IconのSpecについては[Iconography](https://developer.paypay.ne.jp/app-styleguide/globalrule/icongraphy)の項目を参照
    Iconを配置する場合はTitleが複数行の場合も水平方向に中央寄せする

Title / Description / Action Item
![iOS](https://developer.paypay.ne.jp/static/img/list_sect13_images1.69e04789.svg)
![Android](https://developer.paypay.ne.jp/static/img/list_sect13_images2.19a38d70.svg)
    Back ground : 
    **Default**
    Back ground > #FFFFFF
    **Pressed( iOS )**
    Back ground > #F2F2F2
    Divider : 
    **Default**
    #EEEEEE
    1px/dp
    **Error - Edit List**
    #FD5C5C
    1px/dp
    Title : 
    [Body 16 Regular](../globalrule/typography.md)
    Text Align-Left
    #242323
    Description : 
    [Body 16 Regular](../globalrule/typography.md)
    Text Align-Left
    #606060
    Action Item : 
    **Icon**
    24*24px/dp
    **Text-Label**
    [Body 14 Regular](../globalrule/typography.md)
    Text Align-Right
    #606060
    Action Item - Edit List : 
    **Text-Empty**
    [Body 14 Regular](../globalrule/typography.md)
    Text Align-Right
    #BABABA
    **Text-Filled** 
    [Body 14 Regular](../globalrule/typography.md)
    Text Align-Right
    #242323
    Error text - Edit List : 
    **Text-Error**
    [Body 12 Regular](../globalrule/typography.md)
    Text Align-Left
    #FD5C5C
    Margin : 
    8px/dp