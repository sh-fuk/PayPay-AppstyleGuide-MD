# Transition

## Principle
ユーザーアクションによる画面の遷移時には、画面の移動アニメーションを必須とします
アニメーションを提示することによって、ユーザーは自身が現在どの画面を表示しているかを明確にします

## Usage

### Drill Down
ユーザーアクションにより、下の階層へ移動する場合は左から右へのアニメーションを表示し、画面が切り替わったことを明示します。
下層から上層に戻る場合も同様に右から左へのアニメーションを表示します。

![](https://developer.paypay.ne.jp/static/img/transition_sect2_icons1.083e90df.svg)

### Slide UP
現在の動作を一時中断して行う、一時的なタスクを表示する場合はSlide upで画面を表示します。
下層への移動アクションにこのトランジションを利用することは禁止します。

![](https://developer.paypay.ne.jp/static/img/transition_sect2_icons2.271604b8.svg)