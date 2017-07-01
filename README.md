# MQL4-Assert
Simple assertion module for MQL4.


## Install
1. Download Assert.mqh
2. Save the file to /MQL4/Includes/mql4_modules/Assert/Assert.mqh


## Usage
1. Define IS_ASSERT
2. Include Assert.mqh

``` cpp
#define IS_ASSERT
#include <mql4_modules/Assert/Assert.mqh>

double sample(double lots, double price) {
   assert(lots > 0, "invalid parameter lots");

   ...
   ...
}
```
In this case, if lots less than zero or equales zero, displays message.

Note: You need define IS_ASSERT before include assert.mqh.

## Bibliography
- [USING ASSERTIONS IN MQL5 PROGRAMS](https://www.mql5.com/en/articles/1977)
