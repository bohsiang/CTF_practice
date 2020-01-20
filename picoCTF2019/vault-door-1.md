 
# vault-door-1 - Points: 100

### This vault uses some complicated arrays! I hope you can make sense of it, special agent. The source code for this vault is here: [VaultDoor1.java](https://2019shell1.picoctf.com/static/955f5aeef623b09378306dd6c1f88f96/VaultDoor1.java)

這邊就是要考驗逆向的技巧

將檔案打開後會發現裡面是java的語法

在java中charAt是顯示字串位置的方法

所以我們將其組合排列後就能夠得到這題的答案了

```java
public boolean checkPassword(String password) {
        return password.length() == 32 &&
               password.charAt(0)  == 'd' &&
               password.charAt(1)  == '3' &&
               password.charAt(2)  == '5' &&
               password.charAt(3)  == 'c' &&
               password.charAt(4)  == 'r' &&
               password.charAt(5)  == '4' &&
               password.charAt(6)  == 'm' &&
               password.charAt(7)  == 'b' &&
               password.charAt(8)  == 'l' &&
               password.charAt(9)  == '3' &&
               password.charAt(10) == '_' &&
               password.charAt(11) == 't' &&
               password.charAt(12) == 'H' &&
               password.charAt(13) == '3' &&
               password.charAt(14) == '_' &&
               password.charAt(15) == 'c' &&
               password.charAt(16) == 'H' &&
               password.charAt(17) == '4' &&
               password.charAt(18) == 'r' &&
               password.charAt(19) == '4' &&
               password.charAt(20) == 'c' &&
               password.charAt(21) == 'T' &&
               password.charAt(22) == '3' &&
               password.charAt(23) == 'r' &&
               password.charAt(24) == '5' &&
               password.charAt(25) == '_' &&
               password.charAt(26) == '5' &&
               password.charAt(27) == '1' &&               
               password.charAt(28) == 'e' &&
               password.charAt(29) == '7' &&
               password.charAt(30) == 'f' &&
               password.charAt(31) == 'd';                           
    }
```

