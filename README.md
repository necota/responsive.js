Responsive.js
=============
レスポンシブ用の軽量ユーティリティです。  
以下の実装が容易になります。

* リサイズ時に、画面幅が指定した範囲内であれば関数を実行する。
* ブレイクポイントを跨いだ時だけ処理を実行する。
* 画面幅が指定した範囲内かどうかを判定する。

## 使い方

### responsive(min_width, max_width, callback)

```js
responsive(0, 640, function(changed){
  if(!changed) return;
  smartphone_function();
});

responsive(641, 999, function(changed){
  if(!changed) return;
  tablet_function();
});

responsive(1000, null, function(changed){
  if(!changed) return;
  pc_function();
});
```

### matchWidthMediaQuery(min_width, max_width)

```js
jQuery("#sample").on("click", function(){
  if(matchWidthMediaQuery(0, 640)){
    // smartphone
  }else if(matchWidthMediaQuery(641, 999)){
    // tablet
  }else{
    // pc
  }  
});
```


## IE9対応

下記スクリプト追加で対応可能。  
https://github.com/paulirish/matchMedia.js/
