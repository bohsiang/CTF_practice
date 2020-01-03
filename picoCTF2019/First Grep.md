 
# First Grep - Points: 100

### Can you find the flag in file? This would be really tedious to look through manually, something tells me there is a better way. You can also find the file in /problems/first-grep_0_93be1631acf1a93b98cdcc3e7b9fdc52 on the shell server.

利用ssh連線到伺服器在切換到上述路徑下

使用 `ls` 可以發現底下有個檔案， `file` 查看發現他是ascii的檔案
![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/First%20Grep_1.PNG)
![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/First%20Grep_2.PNG)
直接用 `cat` 指令會發現文字非常多找不到flag
![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/First%20Grep_3.PNG)
這邊就可以在後面加上 `grep` 這個參數來限制輸出就可以得到這題的flag了
![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/First%20Grep_4.PNG)

