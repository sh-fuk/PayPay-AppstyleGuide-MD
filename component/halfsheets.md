# Half Sheets

## Usage
* ユーザー操作を一時中断させ、アクションを促す、またはエラーなどのお知らせを表示する際に使用します
* ハーフシートはあくまで副次的な情報を表示するものであり、ハーフシート上に主コンテンツを表示することは推奨しません（Mini-Appは除く）
* ハーフシート上には、表示された理由、ユーザーがとるべきアクションをわかりやすく表示します

### Usage Example
![](https://developer.paypay.ne.jp/static/img/halfsheet_01.f8532321.svg)

## Type
![3枚のハーフシートのスクリーンショット](https://developer.paypay.ne.jp/static/img/halfsheet_02.47657259.svg)

1枚目 : Regular
2枚目 : Date picker
3枚目 : Alternative

## Detail
![ハーフシートのコンポーネントが1-7でマークアップされてる画像](https://developer.paypay.ne.jp/static/img/halfsheet_03.093c2ae3.svg)

1 : 
Image(Option)
ハーフシートに表示されている内容をよりわかりやすく伝えるため、イメージを配置します

**エラーアイコン**
エラーやアラートを表示する場合は、共通のエラーアイコンや機能独自のエラーアイコンを表示します
詳細は[アイコンの項目](../globalrule/iconography.md)をご確認ください

2 : 
Title
タイトルを表示します
タイトルは内容を端的に理解できるよう、簡潔でコンパクトな一文を利用します
文末に句点は使いません

3 : 
Description(Option)
タイトルでは伝えきれない補足情報を表示します
文末に句点は使いません

4 :
Links(Option)
リンクテキストを表示します
主に、ユーザーの同意を得るための利用規約へのリンクやヘルプページへのリンクを表示する場合など
補足的要素に利用し、主要アクションボタンとしての利用は禁止します
リンクは3つまでの表示を推奨します
表示パターンは後述します

5 :
Buttons
アクションボタンを表示します
ボタンは1〜3つまで表示が可能です
ボタンを複数表示する場合は、優先順位を明確にし、ユーザーが次のアクションに迷わないように配慮してください
ボタンの表示パターンは後述します

6 : 
Half sheet background
ハーフシートの背景です
高さは表示コンテンツの内容によって変化します

7 : 
Blur background
ハーフシートの表示時は、黒の透過背景（オーバーレイ）を表示し、下層のコンテンツを認識できるようにします
原則、このエリアをタップすると、ハーフシートを閉じます

ただし、以下の場合は、このエリアをタップしてもハーフシートは閉じないようにします
• ハーフシート上の操作を追えずに閉じることで挙動や表示要素に不整合が起こる場合
• エラー時など、シートを閉じて再度同様の操作をしても結果が変わらない場合

**注意事項**
5. Buttons
ボタンを複数表示する場合は、優先順位を明確にし、ユーザーが次のアクションに迷わないように配慮してください。

[Primary Button](../component/buttons.md)
![ボタンを一つだけ表示（推奨）](https://developer.paypay.ne.jp/static/img/halfsheet_04_01.583cd53b.svg)
![ボタンを2つ表示(推奨) Primary/Secondary](https://developer.paypay.ne.jp/static/img/halfsheet_04_02.9eed2f7c.svg)
![ボタンを3つ表示 Primary/Secondary/Tertiary](https://developer.paypay.ne.jp/static/img/halfsheet_04_03.a3264736.svg)

## Interaction
ボタンアクション時にタップフィードバックを表示します。
[Buttons](../component/buttons.md)を参照してください。
参考: [Interaction](../globalrule/interaction.md)

## Transitions
表示 : スライドアップで表示します
閉じる : スライドダウンで閉じます

## Spec

![ハーフバーの感覚や余白がマークアップされた画像](https://developer.paypay.ne.jp/static/img/halfsheet_05.e2d7d612.svg)

Image (Option) : 128px*64px

Title : 
[Hading 16](../globalrule/typography.md)
Text Align-Center
#242323

Description(Option) : 
[Label 14 Regular](../globalrule/typography.md)
Text Align-Center
#242323

Links(Option) : 
[Label 14 Regular](../globalrule/typography.md)
Text Align-Center
#3895FF

Buttons : [Buttons](../component/buttons.md)

Half sheet background : 
#FFFFFF
TOP Right & Left Round : 20px/dp

Blur background : 
Alpha 0.6
#000000