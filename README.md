# MQL4-Assert
MQL4でアサーションが使いたかったので下部のURLを参考に作成した。  
定義値IS_ASSERTの有無で有効/無効の切り替えが可能。  
有効時には前提条件となる評価式の判定をおこない、結果が偽の場合にはエラーを通知後にプログラムを終了（チャートから除外）する。    
無効時には評価式の判定処理は実行されない。  

## Install
1. download Assert.mqh
2. /MQL4/Include/配下に保存する。

## Usage
1. IS_ASSERTを定義する
2. includeでAssert.mqhを読み込む
3. assert(評価式, エラーコメント); の形式で実行する

``` cpp
#define IS_ASSERT
#include <Assert.mqh>

double sample(double lots, double price) {
   assert(lots > 0, "invalid parameter lots");

   ...
   ...
}
```
この場合lotsが0以下の数値だとエラーコメントが表示されます。

※assertを有効にする場合は、**assert.mqhを読み込む前**にIS_ASSERTを定義して下さい。

## 参考
- [USING ASSERTIONS IN MQL5 PROGRAMS](https://www.mql5.com/en/articles/1977)
