---
title: For which value of x the results of the following statements are not the same?
date: 2017-01-08 14:11:14
tags:
---
For which value of x the results of the following statements are not the same?
```bash
//  if( x <= 100 ) {...}
if( !(x > 100) ) {...}
```
***`Solution`***
`NaN <= 100` is `false` and `NaN > 100` is also `false`, so if the value of `x` is `NaN`, the statements are not the same.

The same holds true for any value of x that being converted to Number, returns `NaN`, e.g.: `undefined`, [1,2,5], `{a:22}` , etc.

This is why you need to pay attention when you deal with numeric variables. NaN can’t be equal, less than or more than any other numeric value, so the only reliable way to check if the value is NaN, is to use `isNaN()` function.