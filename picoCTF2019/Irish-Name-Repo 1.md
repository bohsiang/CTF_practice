 
# Irish-Name-Repo 1 - Points: 300

### There is a website running at https://2019shell1.picoctf.com/problem/27383/ or http://2019shell1.picoctf.com:27383. Do you think you can log us in? Try to see if you can login!

這題是考驗大家SQL injection的技術

從側邊的頁面可以發現有個登入的選項

![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/Irish-Name-Repo%201_1.PNG)

假設亂輸入的話並沒有辦法登入

![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/Irish-Name-Repo%201_2.PNG)

基本上大家若是有使用過SQL來存放資料會知道它寫入的語法

大概會長```"SELECT * FROM 資料表 WHERE 欄位1 = 'data' AND 欄位2 = 'data'"```

那今天要執行SQL injection就是要將其中的欄位作閉合


這題的題目可能為```"SELECT * FROM datasheet WHERE username = 'data' AND password = 'data'"```

我們的目標是使上面的語法永遠成立

那基本上我們要先閉合並且加入一個恆等式後將其它的註解掉

![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/Irish-Name-Repo%201_3.PNG)

在username一定成立的狀況下就可以騙過伺服器了


→→→→ username = '`' or 1=1 -- ` ' AND password = 'data'"


![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/Irish-Name-Repo%201_4.PNG)
