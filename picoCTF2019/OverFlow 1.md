 # OverFlow 1 - Points: 150

### You beat the first overflow challenge. Now overflow the buffer and change the return address to the flag function in this program? You can find it in /problems/overflow-1_4_6e02703f87bc36775cc64de920dfcf5a on the shell server. Source.

這題是要利用buffer overflow的漏洞來return到我們想要的位置上



不管輸入太短的字串都只會看到return到一樣的位置上

![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/OverFlow%201_1.PNG)

看一下程式碼我們希望return到flag() function的位址上才能打開flag.txt

```c
void flag() {
  char buf[FLAGSIZE];
  FILE *f = fopen("flag.txt","r");
  if (f == NULL) {
    printf("Flag File is Missing. please contact an Admin if you are running this on the shell server.\n");
    exit(0);
  }

  fgets(buf,FLAGSIZE,f);
  printf(buf);
}
```

所以我們要將上面圖片的位址轉跳到flag() function的位址

![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/OverFlow%201_2.PNG)

在這邊我先利用r2這個套件來找出其位置



上面就是我們要return的位置

接下來的步驟是找尋需要補多少字元到其位置上

我們可以利用gdb來看剛剛輸入的字元被存放至甚麼地方

![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/OverFlow%201_3.PNG)

接著觀察一下它與return差了多遠實際上差的距離為`0xffffd3fc - 0xffffd3b0` = 76(dec)

![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/OverFlow%201_4.PNG)

![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/OverFlow%201_5.PNG)


所以我們的payload要用76個字元加上我們要return的位置才會跳出flag

![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/OverFlow%201_6.PNG)

![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/OverFlow%201_7.PNG)

