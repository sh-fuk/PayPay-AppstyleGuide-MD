# Layout

## Principle
画面内のコンポーネントの配置や余白を定義します。
異なるプラットフォーム、環境下でも、定義したルールに従って設計することで、すべての環境で一貫性を保ちます。

## Usage
### Margin Rule
画面内で利用する余白は基本的に4の倍数のpx/dpを指定します。

![](https://developer.paypay.ne.jp/static/img/layout_sect2_icons.888e83d6.svg)

ただし、細かいパーツが複雑に組み合わさるコンポーネントなどは、例外を認めます。

## Responsive Layout
特に、スマートフォンWeb/App、タブレット、デスクトップで共通で表示するWebコンテンツを作成する場合は、どのような環境で表示されてもユーザビリティを損ねないレイアウトを用意する必要があります。

次に定義するブレイクポイントによって、 スマートフォン/デスクトップでのレイアウトを切り替えます。タブレットはスマートフォンの延長であると考え、ブレイクポイント は1点だけとします。

![](https://developer.paypay.ne.jp/static/img/layout_sect3_icons.6adbaf59.svg)

## Margin
大きく2種類の余白を定義します。

![余白のポイントスクショ](https://developer.paypay.ne.jp/static/img/layout_sect4_icons.ef723c6a.png)

上記画像1番 : 画面の端から要素の間の余白
上記画像2番 : 要素同士の余白

## 画面の端から要素の間
画面の端からコンテンツの間に余白を設けることで、コンテンツの視認性を担保します。スマートフォンの環境では、余白は24px/16pxを利用します。 余白の使い分けの目安は以下の通りです。

入力フォームやアクションボタンがメインとなる画面

![入力フォームやアクションボタンがメインとなる画面](https://developer.paypay.ne.jp/static/img/layout_sect5_icons1.96dc7db8.svg)
![カードUIやリストがメインコンテンツとなる画面](https://developer.paypay.ne.jp/static/img/layout_sect5_icons2.fbe347ed.svg)

## 環境別の指定
タブレット、デスクトップの環境では、余白は40px/24pxを利用します。
余白の切り替えはブレイクポイントによって行われます。

![](https://developer.paypay.ne.jp/static/img/layout_sect6_icons.95f57284.png)

## 要素同士の余白
複数のコンテンツが隣接する場合はコンテンツの間に十分な余白を設け、近接する情報のグルーピングを明確にします。複数のコンテンツが並ぶ場合は8px / 12px / 16pxの余白の利用を推奨します。

![余白と余白の間のコンポーネントは固定値ではなく、パーセンテージで定義します。余白は固定値として指定し、コンポーネントはデバイスのサイズによって可変とします。](https://developer.paypay.ne.jp/static/img/layout_sect7_icons.10c7962b.png)

## About Safe Area
ノッチやカットアウト領域のあるデバイスでは、Safe Area外へのアクションコンポーネントの配置を禁止とします。
Safe Area外にはビジュアル要素のみの表示を推奨します。
Safe Area外にも背景色や装飾要素を表示することによって、画面を広く見せることができ、より快適な体験を提供することができます。

![iOS/AndroidのSafeArea図](https://developer.paypay.ne.jp/static/img/layout_sect8_icons.b2f68b13.svg)

iOS : iOS Deviceの場合、上部44px、下部34pxの間をSafe Areaとします。[iOS Human Interface Guideline](https://developer.apple.com/design/human-interface-guidelines/ios/visual-design/adaptivity-and-layout)をご覧ください。
Android : Android Deviceの場合、カットアウトエリアのサイズは機種に依存します。Support Display Cutout を参照してください。

セーフエリア内でのアクションコンポーネントの配置
![アクションコンポーネントはSafe Area内に配置する / Do](https://developer.paypay.ne.jp/static/img/layout_sect8_doimage.239947f1.svg)
![アクションコンポーネントをSafe Area外に配置する / Don't](https://developer.paypay.ne.jp/static/img/layout_sect8_dontimage.8156de48.svg)

## Layout Pattern
画面のレイアウトに定形パターンを定義します。
サービスのコンセプトや機能によって使い分けをします。

![番号付きのレイアウトの説明画像5枚](https://developer.paypay.ne.jp/static/img/layout_sect9_icons.e6e58853.svg)

| 番号 | 名前 | 説明 |
| :--- | :--- | :--- |
| 1 | Normal | 最も一般的なレイアウトです。基本的にはこのレイアウトを利用します。 |
| 2 | Section | 1画面に複数のセクションを表示する場合に利用します。セクションごとにまとめられたコンテンツを表示し、情報の区切りを明確にします。 |
| 3 | Card | 1画面に複数のセクションを表示する場合に利用します。セクションごとにまとめられたコンテンツを表示し、情報の区切りを明確にします。カード両端に余白を設けることで、Sectionよりも、カード自体がアクション可能なことを明示します。Cardレイアウトは画面端左右に16pxの余白を設けます。 |
| 4 | Full screen | カメラやプロモーションなど、画面全体にコンテンツを配置する場合に利用します。ヘッダーエリアの背景は透過し、下に配置されるコンテンツが見えるようにします。ヘッダーエリアのテキストは十分に可読性を担保する処理が必要です。 |
| 5 | Half color background | 画面上部に重要な情報を表示する場合に利用します。画面上部にはアイキャッチとなるサービスや機能の特性を表す色を設定します。色の設定についてはFlavor Colorを参照してください。 |

## Aspect Ratios
画面に配置される画像やコンポーネントのアスペクト比を定義します。以下の比率を利用することを推奨します。

![1:1 , 3:4 , 1:1.6 , 1:2](https://developer.paypay.ne.jp/static/img/layout_sect10_icons1.cd616db6.svg)

## Usage Example
![色の使い方の実例](https://developer.paypay.ne.jp/static/img/layout_sect10_icons2.21886ce3.png)x