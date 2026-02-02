# React：MDN学習記録
以下の章の、React に関するページを学習。
- [JavaScript フレームワークとライブラリー | MDN](https://developer.mozilla.org/ja/docs/Learn_web_development/Core/Frameworks_libraries)

## 2/2(月)
以下のページについて
https://developer.mozilla.org/ja/docs/Learn_web_development/Core/Frameworks_libraries/React_accessibility

フォーカスの制御について、`<input ref={inputRef}>` のところが引っかかっているので調べました。

フォーカスを当てるのは1つなのに<input>の数だけinputRefが設定されてしまうのでは？重複してinputRefが設定されても問題ないのかな？と思いましたが、条件つきレンダリングで編集中の`<input>`は1つだけしか表示されないとのことで腑に落ちました。今回のケースは1つだけの設計なので問題ないようです。
