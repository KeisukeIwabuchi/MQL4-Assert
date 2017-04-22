# mql4-assertion
MQL4でアサーションが使いたかったので作った。

## インストール
1. download assert.mqh
2. save this file in \<Your DataFolder\>/MQL4/Include/

## 使い方
1. IS_ASSERTを定義する
2. assert.mqhを読み込む
3. assert(評価式, エラーコメント);の形式で実行する

```
#define IS_ASSERT
#include <assert.mqh>

double sample(double lots, double price) {
   assert(lots > 0, "invalid parameter lots");
   
   ...
   ...
}
```

※assertを有効にする場合は、assert.mqhを読み込む前にIS_ASSERTを定義して下さい。

## 参考 
- [USING ASSERTIONS IN MQL5 PROGRAMS](https://www.mql5.com/en/articles/1977)
