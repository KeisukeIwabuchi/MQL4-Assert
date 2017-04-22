# mql4-assertion
MQL4でアサーションが使いたかったので下記のURLを参考に作成しました。  
定義値IS_ASSERTの有無で有効/無効の切り替えが可能。  
有効時には前提条件となる評価式の判定をおこない、結果が偽の場合にはエラーを通知後にプログラムを終了する。  
無効時には評価式の判定処理は実行されない。  

## インストール
1. download assert.mqh
2. save this file in \<Your DataFolder\>/MQL4/Include/

## 使い方
1. IS_ASSERTを定義する
2. assert.mqhを読み込む
3. assert(評価式, エラーコメント);の形式で実行する

サンプル
```
#define IS_ASSERT
#include <assert.mqh>

double sample(double lots, double price) {
   assert(lots > 0, "invalid parameter lots");
   
   ...
   ...
}
```
この場合lotsが0以下の数値だとエラーコメントが表示されます。

※assertを有効にする場合は、assert.mqhを読み込む前にIS_ASSERTを定義して下さい。

## 参考 
- [USING ASSERTIONS IN MQL5 PROGRAMS](https://www.mql5.com/en/articles/1977)
