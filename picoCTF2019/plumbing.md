 
# plumbing - Points: 200

### Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to ```2019shell1.picoctf.com 18944```.

用`nc`連過去就會發現有一堆不是flag的答案出現

![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/plumbing_1.PNG)

這個時候只要利用`grep`在後面限制只要讀取`pico`相關的文字就可以得到答案了

![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/plumbing_2.PNG)
