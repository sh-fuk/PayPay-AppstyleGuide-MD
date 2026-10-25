# Balloon

## Usage
* 新機能のガイドなど、特定のコンポーネントに補足情報を示す際に使用します
* ユーザーが気付きにくい情報を補足することで、機能やコンポーネントの理解が深まり、より良い体験をもたらします
* Balloonはあくまで補足的な情報の提示のみに使用するものとし、主コンテンツの閲覧やアクションを妨げるような使い方はしません

## Usage Example
![新機能の訴求](https://developer.paypay.ne.jp/static/img/balloon_sect2_images_panel1.6232e7ed.svg)
![新着情報のお知らせ](https://developer.paypay.ne.jp/static/img/balloon_sect2_images_panel2.a5e7ba05.svg)

## Type
Balloonのコンポーネントには2種類あり、用途によって使い分けをします。

![Coach Balloon](https://developer.paypay.ne.jp/static/img/balloon_sect3_images_panel1.5bad009a.svg)
![Scroll Balloon](https://developer.paypay.ne.jp/static/img/balloon_sect3_images_panel2.63ad3139.svg)

Coach Balloon : 新機能などの特定のComponentを強調、ガイドする場合に使用します。
Scroll Balloon : 画面外の特定のComponentをガイドする場合に使用します。Balloonをタップすると対象のComponentの位置まで自動でスクロールします。

## Detail
![1-3の番号がマークアップされたバルーン](https://developer.paypay.ne.jp/static/img/balloon_sect4_images.f7079fdb.png)

1 : Icon (Option) : メッセージやガイドに合わせたアイコンを表示します。アイコンを付与することでよりユーザーの注目を集めることができます。
2 : Text Label : Balloonが示す訴求メッセージやガイドテキストを表示します。ユーザーが瞬時に内容を理解できるよう、簡潔に、1行以内に収まる文字数を推奨します。
3 : Arrow : Balloonの示すComponentの位置に合わせてArrowを配置します。<br>![](https://developer.paypay.ne.jp/static/img/balloon_sect4_col2_images_no3.e72121f7.svg)

## Do / Don't
Coach Balloonを使用する際は、訴求対象が明確になるようにしてください。

![強調したいコンテンツが明確](https://developer.paypay.ne.jp/static/img/balloon_sect5_points1.58767e93.png)
![同一画面に複数のバルーンを配置する。どのComponentが強調されているのか不明瞭](https://developer.paypay.ne.jp/static/img/balloon_sect5_points2.83038994.png)
![Balloonの視認性が悪い。Balloonに近しい背景色の上への配置](https://developer.paypay.ne.jp/static/img/balloon_sect5_points3.76aa5373.png)

## Scroll Balloon
![1-2の番号がマークアップされたScroll Balloon](https://developer.paypay.ne.jp/static/img/balloon_sect6_images.68583621.svg)

1 : Text Label : Balloonが示す訴求メッセージやガイドテキストを表示します。ユーザーが瞬時に内容を理解できるよう、簡潔に、1行以内に収まる文字数を推奨します。
2 : Arrow Animation : 画面下部を示すアイコンアニメーションを表示し、画面外に情報があることを示します。

Scroll BalloonにはPrimary ColorとSecondary Colorがあります。
強調するコンテンツの優先度によって使い分けます。
更新頻度の高いタイムラインコンテンツなど、新着情報を表示する場合は表示されているコンテンツを阻害しないよう、Secondary Colorの利用を推奨します。

画面外の新機能を訴求する場合など
![Primary Color Balloon](https://developer.paypay.ne.jp/static/img/balloon_sect6_rowers_no1.6cd5ee46.svg)

更新頻度の高いタイムラインコンテンツの新着件数の表示など
![Secondary Color Balloon](https://developer.paypay.ne.jp/static/img/balloon_sect6_rowers_no2.549c58da.svg)

## Do / Don't
画面内の主コンテンツの閲覧、アクションの妨げになるような表示は禁止とします。

![テキストが短く簡潔に表示されている / Do](https://developer.paypay.ne.jp/static/img/balloon_sect7_rowers_panel1.a2d9cdc6.svg)
![テキストが改行されているなど、可読性が低い / Don't](https://developer.paypay.ne.jp/static/img/balloon_sect7_rowers_panel2.d71c7427.svg)

## Interaction

Coach Balloon : 特殊な場合を除き、Balloonをタップ、もしくは対象のComponentをタップするとBalloonは非表示となります。アクションを伴わないComponentを訴求する場合は表示回数を設定し、ユーザーアクションを伴わなくともBalloonが非表示になるようにします。表示回数3回ほどで自動非表示にすることを推奨します。
Scroll Balloon : Balloonをタップ、もしくは画面をスクロールするとBalloonは非表示となります。アクション時にタップフィードバックを表示します。Specを参照してください。参考：[Interaction](../globalrule/interaction.md)

## Spec

### Coach Balloon

![](https://developer.paypay.ne.jp/static/img/balloon_sect9_images.9be4555e.svg)

Text Label : [Heading / Label 14](../globalrule/typography.md) : Text Align-Left : Default > #FFFFFF : Pressed( iOS ) > #FFFFFF, Alpha 0.7
Background : Default > #00B9F5 : Pressed( iOS ) > #00AFE8 : Shadow > [Low-shadow](../globalrule/shadow.md)

### Scroll Balloon

![](https://developer.paypay.ne.jp/static/img/balloon_sect10_images.43616d6e.svg)

Text Label（Primary）: [Heading / Label 14](../globalrule/typography.md) : Text Align-Left : Default > #FFFFFF : Pressed( iOS ) > #FFFFFF, Alpha 0.7
Text Label（Secondary）: [Heading / Label 14](../globalrule/typography.md) : Text Align-Left : Default > #00B9F5 : Pressed( iOS ) > #00B9F5, Alpha 0.7

Background（Primary）: Default > #00B9F5 : Pressed( iOS ) > #00AFE8 : Shadow > [Low-shadow](../globalrule/shadow.md)
Background（Secondary）: Default >  : Back ground > #FFFFFF : Pressed( iOS ) >  : Back ground > #F2F2F2 : Shadow > [Low-shadow](../globalrule/shadow.md)


## 画面下部からの距離

ボトムタブがある場合 : 16px/dp
ボトムタブがない場合 : 40px/dp