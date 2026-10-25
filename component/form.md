# Form

## Usage
* ユーザーが任意のテキストを入力する際に使用します
* 入力するべき内容や入力可能な文字数など、ユーザーが入力に必要な情報をわかりやすく表示します
* ユーザーが現在の状態を直感的に認識できるよう、入力前・入力済み・エラーなど、状態ごとに視覚的な差をつけて明示します

### Usage Example
![短文と長文の例](https://developer.paypay.ne.jp/static/img/form_sect1_images1.3b04b757.svg)

## Type
![入力エリアの高さ固定（短文）](https://developer.paypay.ne.jp/static/img/form_sect2_images1.688991c4.svg)
![入力エリアの高さ可変（長文）](https://developer.paypay.ne.jp/static/img/form_sect2_images2.e301a6db.svg)

## Detail
![フォームに1-6のマークアップ](https://developer.paypay.ne.jp/static/img/form_sect3_images.596e9c45.svg)

1 : 
Title (Option)
入力するべき項目を表示します。
ユーザーが適切な回答を入力できるよう、簡潔なテキストを原則とします。

2 / 3: 
Text Field / Message Area
ユーザーが回答を入力するエリアです。
Text Fieldにフォーカスをあてるとキーボードが表示されます。
入力項目についての補足、または入力項目にエラーがある場合はMessage areaにメッセージを表示します

### ステータス別の表示

入力エリアがEmptyの場合は、何を入力するべきかを示す必要があります
Place holderを利用して、入力例や入力項目名を表示します
入力項目についての補足情報がある場合は、Message areaに表示します
![Empty](https://developer.paypay.ne.jp/static/img/form_sect7_icons1.5bc96f2b.svg)

ユーザーの入力した文字列が表示されます
アクティブな状態を表すために、入力エリアの下線部を青色 かつ 太線で表示します
入力エリアに1文字以上テキストが入力されている場合、Action itemの削除ボタンを表示します
![Editing](https://developer.paypay.ne.jp/static/img/form_sect7_icons2.5418e3f6.svg)

入力済み かつ キーボードのフォーカスが外れている場合は入力エリアの下線部を青色で表示します
![Filled](https://developer.paypay.ne.jp/static/img/form_sect7_icons3.5bf75b1d.svg)

ユーザーの入力に誤りがある場合は入力エリアをエラー色で表示し、入力値が不正であることを明示します
同時に、ユーザーがエラーの理由を理解できるよう、Message areaにエラーメッセージを表示します
![Error](https://developer.paypay.ne.jp/static/img/form_sect7_icons4.b6ee7bbb.svg)

入力不可能なことを明示します
入力エリア下線部の色をグレーアウトし、操作が不可能だということを明示します
Place holderまたは入力値が表示されます
![Non-Editable](https://developer.paypay.ne.jp/static/img/form_sect7_icons5.2ee9911a.svg)


4 :
Action Item

入力エリアに1文字以上テキストが表示されている場合、必ず表示します
タップすると、入力した文字列はすべて削除されます
![削除*必須](https://developer.paypay.ne.jp/static/img/form_sect8_icons1.e8d14ef1.svg)

入力内容を記号に置き換えた不可視状態と可視状態を切り替えることができます
パスワードなど機密性の高い項目を入力する際に使用します
可視・不可視の状態が認識できるよう、アイコンの表示も切り替えます
不可視状態をデフォルト表示とします
不可視状態で入力すると、入力した文字列は「●」に置き換えられて表示されます
![不可視 *任意](https://developer.paypay.ne.jp/static/img/form_sect8_icons2.5b0a3703.svg)
![可視 *任意](https://developer.paypay.ne.jp/static/img/form_sect8_child_icons2.a8cbf308.svg)

5 : 
Text Counter (Option)
入力中の文字数と上限文字数を表示します。
入力と同時に文字数をリアルタイムで反映します。
入力文字数が上限を超えた場合、Message areaにエラーを表示します。

![入力文字数が上限以内](https://developer.paypay.ne.jp/static/img/form_sect9_images1.a0b62402.svg)
![入力文字数が上限以上](https://developer.paypay.ne.jp/static/img/form_sect9_images2.19232ffe.svg)

## Interaction

Empty時にText Fieldをタップ
キーボードが表示され、TextFieldがEditable表示に切り替わる
キーボードの表示アニメーションは端末の仕様に準拠
![入力中表示](https://developer.paypay.ne.jp/static/img/form_sect10_images1.c669e42f.svg)

入力エリアの高さ可変あり
長い文字列を入力する場合、Text Fieldが文量に合わせて下に広がる
![可変](https://developer.paypay.ne.jp/static/img/form_sect10_images2.1ca858c4.svg)

## Spec
![フォームに余白や間隔などのpxがマークアップされている画像](https://developer.paypay.ne.jp/static/img/form_sect11_images.e57feed7.svg)

Title (Option) :
[Label 12 Regular](../globalrule/typography.md)
Text Align-Left
#606060

Text Field - Input Text : 
**Place holder**
[Label 16 Regular](../globalrule/typography.md)
Text Align-Left
#BABABA

**Input**
[Label 16 Regular](../globalrule/typography.md)
Text Align-Left
#242323

Text Field - Form bar : 
**Empty**
1px/dp
#BABABA

**Filled**
1px/dp
#3895FF

**Editing**
2px/dp
#3895FF

**Error**
1px/dp
#FD5C5C

**Non-Editable**
1px/dp
#EEEEEE

Message area : 
**Normal**
[Label 12 Regular](../globalrule/typography.md)
Text Align-Left
#606060

**Error**
[Label 12 Regular](../globalrule/typography.md)
Text Align-Left
#FD5C5C

Action Item : 
**Icon size**
24*24px/dp
**アイコン間のSpacing**
0px/dp

Text Counter (Option) : 
[Label 12 Regular](../globalrule/typography.md)
Text Align-Right
#606060