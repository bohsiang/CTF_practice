 
# Irish-Name-Repo 1 - Points: 300

### There is a website running at https://2019shell1.picoctf.com/problem/27383/ or http://2019shell1.picoctf.com:27383. Do you think you can log us in? Try to see if you can login!

這題是考驗大家SQL injection的技術

從側邊的頁面可以發現有個登入的選項

基本上大家若是有使用過SQL來存放資料會知道它寫入的語法

大概會長```"SELECT * FROM 資料表 WHERE 欄位1 = 'data' AND 欄位2 = 'data'"```

納今天要執行SQL injection就是要將其中的欄位作閉合

這題的題目可能為```"SELECT * FROM datasheet WHERE username = 'data' AND password = 'data'"```

我們的目標是使上面的語法永遠成立


