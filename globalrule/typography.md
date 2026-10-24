# Typography

## Principle
* アプリ内では定義されたタイポグラフィ以外のものは利用しません。定義されたFont Familyを利用し、すべての画面において一貫性を保ちます
* 視認性/可読性を担保し、どんな人が見ても内容を理解できるようにレイアウトする必要があります
* 和文はシステムフォント、欧文はカスタムフォントを利用し、必要以上の装飾やカスタムフォントの利用はしません
* PayPayアプリはあらゆる言語をサポートする必要があります（2020年時点では日本語/英語をサポート）

## Usage
### Font Families

Font Familyはここに定義されたもののみを利用します。
| | iOS | Android | Web |
| :--- | :--- | :--- | :--- |
| **Japanese** | Hiragino Sans | Noto Sans CJK | Sans serif |
| **English** | Graphik | Graphik | Graphik |
| **Number** | Graphik | Graphik | Graphik |
| **Number_Price** | Graphik | Graphik | Graphik |
| **Symbol** | Graphik | Graphik | Graphik |

### Weight
| | Regular | Bold |
| :--- | :--- | :--- |
| **Hiragino Sans** | W3 | W6 |
| **Noto Sans CJK** | Medium | Bold |
| **Graphik** | Medium | Semibold |

### Font Size
フォントサイズはHeading/Label/Bodyの3種類を定義します。
すべてのコンポーネントはこの3種類から構成されます。
各コンポーネントで使われるフォントについては、各ガイドラインを参照してください。

![各コンポーネント上にどのフォントサイズ種別かをマークアップした画像](https://developer.paypay.ne.jp/static/img/typography_01.c994c0cb.png)

### Heading (H)
中見出し、アクションコンポーネント、補足情報に利用します。
9、10pxなどの小さいサイズでは、Boldの利用を推奨します。
11px以下のサイズは主要なコンポーネントには利用しません。

| 項目 | 内容 |
| :--- | :--- |
| **Size** | 14 px / 16px / 18px / 20px |
| **Weight** | Bold |

### Label (L)
ヘッダーやタイトルに利用します。
Head / TitlesのサイズはLabel/Paragraphのサイズより小さくすることはできません。

| 項目 | 内容 |
| :--- | :--- |
| **Size** | 9px / 10px / 11 px / 12px / 14px / 16px |
| **Weight** | Regular/Bold |

### Body (B)
ユーザーアクションによる入力情報、記事、コンテンツの説明文などに利用します。
原則14pxの利用を推奨しますが、重要なコンポーネントについては、16pxを使用する必要があります。

| 項目 | 内容 |
| :--- | :--- |
| **Size** | 12px / 14px / 16px |
| **Weight** | Regular |

### Line Height
Line heightを定義します。
十分な行間を保つことで、テキストの可読性を担保します。

Font size *1.5 px/sp = line-height (vertically centered)

![Example 1](https://developer.paypay.ne.jp/static/img/typography_02.89ffa464.svg)
![Example 2](https://developer.paypay.ne.jp/static/img/typography_03.102da092.svg)

## Size Line-UP
前述の項目で定義したフォントのサイズLine-upです。

Japanese / Bold
| サイズ | 詳細 |
| :--- | :--- |
| **あ 20** | Size 20px / Height 30px<br>Heading |
| **あ 18** | Size 18px / Height 27px<br>Heading |
| **あ 16** | Size 16px / Height 24px<br>Heading/Label |
| **あ 14** | Size 14px / Height 21px<br>Heading/Label |
| **あ 12** | Size 12px / Height 18px<br>Label |
| **あ 11** | Size 11px / Height 16.5px<br>Label |
| **あ 10** | Size 10px / Height 15px<br>Label |
| **あ 9** | Size 9px / Height 13.5px<br>Label |

English / Bold
| サイズ | 詳細 |
| :--- | :--- |
| **A 20** | Size 20px / Height 30px<br>Heading |
| **A 18** | Size 18px / Height 27px<br>Heading |
| **A 16** | Size 16px / Height 24px<br>Heading/Label |
| **A 14** | Size 14px / Height 21px<br>Heading/Label |
| **A 12** | Size 12px / Height 18px<br>Label |
| **A 11** | Size 11px / Height 16.5px<br>Label |
| **A 10** | Size 10px / Height 15px<br>Label |
| **A 9** | Size 9px / Height 13.5px<br>Label |

Japanese / Regular
| サイズ | 詳細 |
| :--- | :--- |
| **あ 16** | Size 16px / Height 24px<br>Label/Body |
| **あ 14** | Size 14px / Height 21px<br>Label/Body |
| **あ 12** | Size 12px / Height 18px<br>Label/Body |
| **あ 11** | Size 11px / Height 16.5px<br>Body |

English / Regular
| サイズ | 詳細 |
| :--- | :--- |
| **A 16** | Size 16px / Height 24px<br>Label/Body |
| **A 14** | Size 14px / Height 21px<br>Label/Body |
| **A 12** | Size 12px / Height 18px<br>Label/Body |
| **A 11** | Size 11px / Height 16.5px<br>Body |

## Text Color
用途別のテキストカラーを定義します。
カラーはカラーパレットから引用しています。
下記に定義されたカラーを異なる用途で利用することは禁止します。

### Default text
TextBlack : #242323
Secondary TextGray : #606060
SubtextGray（PayPay残高で支払いなど）: #909090
Empty/Disabled TextGray（ここにメモを記入など）: #BABABA
TextNavy : #002970

### Status
ErrorTextRed（残高が不足しています）: #FD5C5C
SuccessTextGreen（完了）: #20BF7A
CautionTextYellow : #FFB900
LinkTextBlue（詳細を見る）: #3895FF

## Price Text
PayPayはサービスの特性から、UI上で価格＋円の組み合わせを多用します。
価格は決済アプリにおいて最も重要な情報であり、十分な可読性を担保する必要があります。
価格部分を読みやすくするよう「円」は価格のサイズより小さく表示する必要があります。

ここでは価格と円の比率を定義します。

| Size | Rule |
| :--- | :--- |
| 24〜 | 価格に対し「円」は1/2のサイズを用います<br>例：価格が72pxのとき、「円」は36pxを用います |
| 14〜22 | 価格のサイズに関わらず「円」は12pxを用います |
| 12 | 価格のサイズに関わらず「円」は11pxを用います |