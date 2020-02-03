# picobrowser - Points: 200

### This website can be rendered only by picobrowser, go and catch the flag! https://2019shell1.picoctf.com/problem/12255/ or http://2019shell1.picoctf.com:12255

直接點選flag會發現她跑出一段文字主要是有些東西不符合的狀況發生

![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/picobrowser_1.PNG)

去查看Header會發現這是`user-agent`的欄位

![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/picobrowser_2.PNG)

所以只要將其改為題目所要求的`picobrowser`就可以得到flag了

```curl -A "User-Agent:picobrowser" http://2019shell1.picoctf.com```

這邊我也是使用curl來送我的資訊

![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/picobrowser_3.PNG)
