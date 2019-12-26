 # Glory of the Garden - Points: 50
 
This garden contains more than it seems. You can also find the file in /problems/glory-of-the-garden_0_25ece79ae00914856938a4b19d0e31af on the shell server.


使用ssh or 官方給的shell

cd 到上述目錄底下

直接用```cat```會有一堆亂碼

所以要先用```strings```找出裡面的字串

接著利用```grep "word"```僅侷限於flag的字串就能找到了

![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/Glory%20of%20the%20Garden.png)
