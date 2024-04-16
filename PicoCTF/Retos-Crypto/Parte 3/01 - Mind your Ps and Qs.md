## Objetivo
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/2604f8b51a5cc62d38a3736938f19cef/values)
## Solución
```
┌──(kali㉿kali)-[~]
└─$ cat values
Decrypt my super sick RSA:
c: 861270243527190895777142537838333832920579264010533029282104230006461420086153423
n: 1311097532562595991877980619849724606784164430105441327897358800116889057763413423
e: 65537                                                                             
┌──(kali㉿kali)-[~]
└─$ python    
Python 3.11.8 (main, Feb  7 2024, 21:52:08) [GCC 13.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> from Crypto.Util.number import long_to_bytes
>>> from Crypto.Util.number import inverse
>>> p = 1955175890537890492055221842734816092141
>>> q = 670577792467509699665091201633524389157003
>>> n = p*q
>>> e = 65537 
>>> c = 861270243527190895777142537838333832920579264010533029282104230006461420086153423
>>> 
>>> tn = (p-1) * (q-1)
>>> 
>>> d = pow(e, -1, tn)
>>> 
>>> m = pow(c, d, n)
>>> 
>>> m
13016382529449106065927291425342535437996222135352905256639573959002849415739773
>>> long_to_bytes(m)
b'picoCTF{sma11_N_n0_g0od_13686679}'
>>> 


```
## Notas adicionales

## Referencias