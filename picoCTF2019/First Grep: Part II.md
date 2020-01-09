 
# First Grep: Part II - Points: 200

### Can you find the flag in /problems/first-grep--part-ii_5_956980126dc47c50540b0f8f35a8e443/files on the shell server? Remember to use grep.


這題在強化對```grep```的使用

到路徑下會發現files目錄下有一堆file

那我們還要一個一個進去用```strings```找相關的字串嗎?

其實不必那麼麻煩只要切換到源頭目錄下```grep -r "pico"```就可以得到答案了

![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/First%20Grep2.PNG)
