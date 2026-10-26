# Toast

## Principle
* ユーザーアクションの結果をフィードバックするために利用します
* フィードバックを提示することで、ユーザーは自身のアクションの成功/失敗を知ることができます
* トーストで伝える内容は簡潔で明快な必要があります

## Usage

### Usage Example
![トーストの使用例](https://developer.paypay.ne.jp/static/img/toast_01.ec906f4a.svg)

## Animation
トーストはユーザーに結果を伝えるためだけのものです。
結果のフィードバックが完了した後は、他のコンテンツを阻害しないように、自動的に消す必要があります。

## 禁止事項
![アクションアイテムを加えることは禁止します](https://developer.paypay.ne.jp/static/img/toast_03.4687f71f.svg)
![2行以上の文字を表示することは禁止します](https://developer.paypay.ne.jp/static/img/toast_04.a4e5aa1c.svg)

## Spec
![具体的なトーストのpx数](https://developer.paypay.ne.jp/static/img/toast_05.ac58a872.svg)
![Safe areaのあるデバイスではSafe area外にも背景色を表示します](https://developer.paypay.ne.jp/static/img/toast_06.bee9a7e6.svg)

Font : 
[Heading / Label/14](../globalrule/typography.md)
Text Align-Left
#FFFFFF

Background : #3895FF

Animation : 
Slide up
Stay 1.5 seconds
Slide down