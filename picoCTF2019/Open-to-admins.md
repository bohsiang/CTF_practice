 
# Open-to-admins - Points: 200
 
### This secure website allows users to access the flag only if they are admin and if the time is exactly 1400. https://2019shell1.picoctf.com/problem/49858/ or http://2019shell1.picoctf.com:49858


這題基本上跟登入的問題很相似

只是加入一個新的Cookies需要再送到flag裡面

當然要送cookies的方式有很多我這邊是用curl送

```curl -b "admin=True;time=1400;" http://2019shell1.picoctf.com:49858/flag```

![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/Open-to-admins_1.PNG)

我也有看到其他人是用[EditThisCookie](https://chrome.google.com/webstore/detail/editthiscookie/fngmhnnpilhplaeedifhccceomclgfbg?hl=zh-TW)這套件送


![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/Open-to-admins_2.PNG)

基本上都可以能得到flag就好了

