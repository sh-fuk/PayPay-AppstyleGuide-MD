# Iconography

## Principle
アイコンを利用することで、コンテンツの直感的な理解を促します。
アイコンは単体でも機能する必要があります。テキストを利用しなくても一目で意味が理解できるものである必要があります。
無駄な装飾は排除し、シンプルかつフレンドリーな設計である必要があります。

無駄な装飾をすべて排除し、シンプルに表現
![シンプルな表現](https://developer.paypay.ne.jp/static/img/igrphy_sect1_doimage.20538bea.svg)

立体的な表現、手描きのような表現、有機的な形状は禁止とする
![複雑な表現](https://developer.paypay.ne.jp/static/img/igrphy_sect1_dontimage.ff9acfb9.svg)

## Usage
### Usage Example
![1-4の番号が振られたスクショ4枚](https://developer.paypay.ne.jp/static/img/igrphy_sect2_usages.45400918.svg)

| 番号 | 画面名 | 使うアイコン | 説明 |
| :--- | :--- | :--- | :--- |
| 1 | Home | Service icon | 機能やサービスを表す |
| 2 | List | System icon | メニューの内容を補足する |
| 3 | Header | System icon | アイコン単体で機能を表す |
| 4 | Half sheet | System icon + Status Mark | ハーフシートの内容を補足する |

## Type
アイコンのTypeによって、利用する色が異なります。

### Service Icon
PayPayの機能やサービスを表すアイコンです。
基本の紺色の他に、サービスのイメージに近い1色をカラーパレットから選定し利用します。
色の選定についてはSpecを参照ください。

![サービスアイコン12種の例](https://developer.paypay.ne.jp/static/img/igrphy_sect3pnel_img1.6d5a4f41.svg)

### System Icon
アプリの機能や操作などに利用されるアイコンを指します。
単色または紺色と青色の２色を使います。

![システムアイコン12種の例](https://developer.paypay.ne.jp/static/img/igrphy_sect3pnel_img2.a2f92ad1.svg)

### Status Mark
System IconにStatus Markを組み合わせることで、状態を表すことができます。
ハーフシートや操作の説明時に利用します。
組み合わせることで視認性が損なわれる場合は利用せず、視認性が十分に担保できるサイズで利用してください

![基になるシステムアイコンとそれのステータスマークの例](https://developer.paypay.ne.jp/static/img/igrphy_sect3pnel_img3.1782b921.svg)

| 番号 | 意味 | 説明 |
| :--- | :--- | :--- |
| 1 | Success / 成功 | アクションが完了し、処理が成功した際に表示します |
| 2 | Add New / 追加 | 追加アクションの確認、実行時に表示します |
| 3 | Invalid / 無効 | 無効アクションの確認、実行時に表示します |
| 4 | Delete / 削除 | 削除アクションの確認、実行時に表示します |
| 5 | Error / エラー | エラー時、アラート時に表示します |

## Spec
Status Mark

| 名 | 説明 |
| :--- | :--- |
| Icon Size | 24px * 24px |
| Outline | 3px |
| Shape | Round 1px / 2px |
| Template | テンプレートはAiデータで提供しています。テンプレートデータ内には、形状に沿ったガイドが設定してあります。作成するアイコンの形状に近いガイドを目安に作成をしてください。<br>テンプレートについてはTemplateの項目を参照ください。 |

## Color

### Service Icon
以下のColor paletteから色を選択します。

Main Color : #002970 : メインカラーとして共通で紺色を使用します

Accent Color : #00B9F5 , #FFB900 , #20BF7A , #FD5C5C : モチーフの一部にアクセントカラーを使用します。左記4色の中からサービスのイメージにあう色を利用します

### System Icon
以下のColor paletteから色を選択します。

#002970 , #3895ff : System Iconは左記2色の組み合わせ、または単色で利用します

### Don't
![指定色以外の利用は禁止とする](https://developer.paypay.ne.jp/static/img/igrphy_sect5_dontdoimage.caf34aa2.svg)

## Template
アイコンを制作する際は、テンプレート（Ai）での作業を推奨します。
テンプレートは実寸の2倍サイズで展開しています。
Aiファイルで作業した後、Sketch/Figmaで作業する際には1/2サイズに縮小してください。

| 番号 | 意味 | 説明 |
| :--- | :--- | :--- |
| 1 | Padding | アイコン作成エリアには周囲に2pxの余白を設けます。メインとなるアイコンのモチーフはPaddingエリアには配置しません |
| 2 | Icon area | Padding area内（20p*20px）のエリアにメインとなるアイコンのモチーフを配置します |

## 注意事項
作成サイズは実寸の2倍サイズで展開する必要があります。

|  | 表示サイズ | 作成サイズ |
| :--- | :--- | :--- |
| Icon size | 24px*24px | 48px*48px |
| Padding | 2px | 4px |
| Icon area | 20px*20px | 40px*40px |
| Outline | 1.5px | 3px |
| Round | 1px/2px | 2px/4px |

## 基本の形状
テンプレートデータ内には、いくつかの形状に沿ったガイドが設定してあります。
作成するアイコンの形状に近いガイドを目安に作成をしてください。

![](https://developer.paypay.ne.jp/static/img/igrphy_sect7_images.a72f7ccb.svg)

## テンプレートのダウンロード
![こちら](https://developer.paypay.ne.jp/file/icon_tmp.ai)