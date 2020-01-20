 
# whats-the-difference - Points: 200

### Can you spot the difference? [kitters](https://2019shell1.picoctf.com/static/473cf765877f28edf95140f90cd76b59/kitters.jpg) [cattos](https://2019shell1.picoctf.com/static/473cf765877f28edf95140f90cd76b59/cattos.jpg). They are also available at /problems/whats-the-difference_0_00862749a2aeb45993f36cc9cf98a47a on the shell server

這題只要寫一個程式將其不一樣的部分print出來

就可以拿到flag了

```python
kitters = open(path + "kitters.jpg","r").read()
cattos = open(path + "cattos.jpg","r").read()
s = ""

for i,j in zip(kitters,cattos):
    if i != j:
        s += j
print (s)

```
flag = picoCTF{th3yr3_a5_d1ff3r3nt_4s_bu773r_4nd_j311y_aslkjfdsalkfslkflkjdsfdszmz10548}

