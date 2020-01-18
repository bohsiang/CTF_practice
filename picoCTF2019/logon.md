 
# logon - Points: 100

### The factory is hiding things from all of its users. Can you login as logon and find what they've been looking at? https://2019shell1.picoctf.com/problem/45163/ or http://2019shell1.picoctf.com:45163

當點上面網址後就會看到一個網站要登錄進去拿flag

先試試看SQL injection的方式有沒有辦法拿到

發現進去之後並沒有顯示

![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/logon_1.PNG)

那我們就需要來看看有沒有其他東西可以繞過

去檢查一下他的header有沒有資訊

![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/logon_2.PNG)

發現不管輸入甚麼帳號密碼

cookies內的`admin=False` 這個狀況都是一樣的

那我們就試試看利用`curl`送cookies進去看看```curl -b admin=True web_url```

![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/logon_3.PNG)

吐回來的response有一個flag就是這題的答案

![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/logon_4.PNG)
