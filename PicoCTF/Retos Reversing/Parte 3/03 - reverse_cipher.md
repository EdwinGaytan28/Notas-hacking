## Objetivo
We have recovered a [binary](https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev) and a [text file](https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev_this). Can you reverse the flag.
## Solución
```
edwin2809-picoctf@webshell:~$ nano bandera.py
edwin2809-picoctf@webshell:~$ python bandera.py
picoCTF{w1{1wq8/7376j.:}
r3v3rs312528e05
edwin2809-picoctf@webshell:~$ 

cifrado = open('rev_this','r').read()  
print(cifrado)  
  
flag = ''  
  
for i in range(8, len(cifrado)-1):  
       if i & 1 == 0:  
               flag +=chr(ord(cifrado[i])-5)  
       else:  
               flag += chr(ord(cifrado[i])+2)  
  
print(flag)

picoCTF{r3v3rs312528e05}
```
## Notas adicionales

## Referencias