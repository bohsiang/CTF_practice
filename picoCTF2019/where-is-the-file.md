# where-is-the-file - Points: 200

### I've used a super secret mind trick to hide this file. Maybe something lies in /problems/where-is-the-file_6_8eae99761e71a8a21d3b82ac6cf2a7d0.

這題在考驗是否會操作基本指令

切換到目錄底下會發現利用`ls`指令看不到任何東西表示有東西被隱藏起來了

我們只需在ls後面加上-a就能夠看的到隱藏的檔案

![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/where-is-the-file_1.PNG)

知道檔名後就能夠直接用`cat`指令查看內容

![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/where-is-the-file_2.PNG)
