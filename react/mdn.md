# React：MDN学習記録
以下の章の、React に関するページを学習。
- [JavaScript フレームワークとライブラリー | MDN](https://developer.mozilla.org/ja/docs/Learn_web_development/Core/Frameworks_libraries)

（2026年2月からGihhubでの記録を開始しましたが、学習は以前からしていました。そのため記録は中途半端なところからスタートしています）

## 2026/02/02(月)
学習時間：30分  
  
以下のページについて
https://developer.mozilla.org/ja/docs/Learn_web_development/Core/Frameworks_libraries/React_accessibility

フォーカスの制御について、`<input ref={inputRef}>` のところが引っかかっているので調べました。

フォーカスを当てるのは1つなのに<input>の数だけinputRefが設定されてしまうのでは？重複してinputRefが設定されても問題ないのかな？と思いましたが、条件つきレンダリングで編集中の`<input>`は1つだけしか表示されないとのことで腑に落ちました。今回のケースは1つだけの設計なので問題ないようです。

## 2026/02/03(火)
学習時間：30分  

`<input ref={inputRef}>` で、`ref={inputRef}` は通常「refに`{inputRef}` を代入する」となりそうなのに、「`<input>` の DOM ノードを `inputRef.current` に入れる」となるのか疑問でした。

Reactではrefが「特別に解釈するキー」で、仕様で上記のような挙動になるとのことでした。
