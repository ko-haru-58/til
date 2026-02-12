# React：MDN学習記録
以下の章の、React に関するページを学習。
- [JavaScript フレームワークとライブラリー | MDN](https://developer.mozilla.org/ja/docs/Learn_web_development/Core/Frameworks_libraries)

（2026年2月からGihhubでの記録を開始しましたが、学習は以前からしていました。そのため記録は中途半端なところからスタートしています）

## 2026/02/12(木)
学習時間：30分  

useRef() と useEffect() について、ドキュメントを作成してまとめました。

## 2026/02/10(火)
学習時間：30分  

引き続きusePrevious() について。

usePrevious() が難しいというよりも、該当の関数に含まれている useRef() と useEffect() の方でつまづいているような気がしてきました。

```
function usePrevious(value) {
  const ref = useRef();
  useEffect(() => {
    ref.current = value;
  });
  return ref.current;
}
```
https://developer.mozilla.org/ja/docs/Learn_web_development/Core/Frameworks_libraries/React_accessibility
<br>
より
<br><br>
次回は理解のためにこれまで出てきたフックをメモにまとめるところから始めるつもりです。

## 2026/02/05(木)
学習時間：30分  

usePrevious() の中にuseEffect() がある場合について確認中です。

usePrevious() はレンダリングの前の状態を保持するために使うものなのですが、usePrevious(){...}と書かれたときの{...}内の関数のことがよく分かっていないので、調べます。

## 2026/02/04(水)
学習時間：30分

useEffect() について「レンダリングのあとに実行したい関数を呼び出せる」と学習したのですが、その理解だけでは動きが分からず。どうやら思っていたよりももっと色々あって複雑なものみたいです。

## 2026/02/03(火)
学習時間：30分  

`<input ref={inputRef}>` で、`ref={inputRef}` は通常「refに`{inputRef}` を代入する」となりそうなのに、「`<input>` の DOM ノードを `inputRef.current` に入れる」となるのか疑問でした。

Reactではrefが「特別に解釈するキー」で、仕様で上記のような挙動になるとのことでした。

## 2026/02/02(月)
学習時間：30分  
  
以下のページについて
https://developer.mozilla.org/ja/docs/Learn_web_development/Core/Frameworks_libraries/React_accessibility

フォーカスの制御について、`<input ref={inputRef}>` のところが引っかかっているので調べました。

フォーカスを当てるのは1つなのに<input>の数だけinputRefが設定されてしまうのでは？重複してinputRefが設定されても問題ないのかな？と思いましたが、条件つきレンダリングで編集中の`<input>`は1つだけしか表示されないとのことで腑に落ちました。今回のケースは1つだけの設計なので問題ないようです。
