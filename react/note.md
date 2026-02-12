# Note
自分用の覚書です。

## useRef()
useRef()は、Reactコンポーネントで再レンダリングを発生させずに、値を保持したり、DOM要素へ直接アクセスしたりするためのフック。

> // 変数名 = useRef(初期値)  
> const ref = useRef(initialValue)  
>  
> 値の取り出し、変更
>    
> // 設定した値を取り出す  
> const value = ref.current;
>   
> // 値を変更する  
> const ref.current = 2;  
>  
> 引用元  
> https://qiita.com/cheez921/items/9a5659f4b94662b4fd1e

## useEffect()
> useEffectはReactフックの1つであり、コンポーネントがレンダリングされた後に、何らかの副作用を実行するために使用されます。例えば外部からコンポーネントへAPIデータの取得、DOMの操作、コンポーネント内にタイマーを設置したい場合などに利用します。これは、コンポーネントが画面に表示された後に、何らかの処理の実行を操作することができることを意味します。
>
> プログラミングにおいての副作用とは、計算や関数の実行結果が、主たる目的以外に生じる影響のことを指します。
>
> 引用元  
> https://envader.plus/article/444

> useEffect(callbackFn, [dependencies]);
>    
> 第1引数：コールバック関数  
> 第2引数：依存関係の配列。必須ではない。コールバック関数は、この配列のいずれかの値が変更されたときに実行されます。  
>
> 引用元  
> https://kinsta.com/jp/blog/react-useeffect/
