 
# dont-use-client-side - Points: 100

### Can you break into this super secure portal? https://2019shell1.picoctf.com/problem/37893/ or http://2019shell1.picoctf.com:37893

先隨便試試看發現沒有辦法輕易地進去

直接F12檢查原始碼看看

發現要符合JS的條件才有辦法觸發

接著看到split=4代表每四個字元為一組

依照split的乘數進行排列組合就可以得到flag了
