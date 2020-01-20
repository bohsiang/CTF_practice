# vault-door-3 - Points: 200

### This vault uses for-loops and byte arrays. The source code for this vault is here: [VaultDoor3.java](https://2019shell1.picoctf.com/static/cf3e86645522f831c58dba985b23dc04/VaultDoor3.java)

這題是要重組字串來拿到flag

從題目看總長是32個字而輸入的字串最後要跟"jU5t_a_sna_3lpm11ga4e_u_4_m9rf48"這組一樣

所以我們可以用這組字串來反推利用自己熟悉的程式語言

這邊我是使用python將下面的程式在跑一次後就能求到答案

```python
s = "jU5t_a_sna_3lpm11ga4e_u_4_m9rf48"
ans = ["0"]*32

for i in range(0,8):
    ans[i] = s[i]
for i in range(8,16):
    ans[i] = s[23 - i]    
for i in range(16,32,2):
    ans[i] = s[46 - i]
for i in range(31,16,-2):
    ans[i] = s[i]

print("".join(ans))
```

#### flag=picoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_e9af18}
