## Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/15/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/15/level2.flag.txt.enc) in the same directory too.
## Solución
```
edwin2809-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/15/level2.py
--2024-03-03 23:17:27--  https://artifacts.picoctf.net/c/15/level2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.92, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 914 [application/octet-stream]
Saving to: 'level2.py'

level2.py                                               100%[===============================================================================================================================>]     914  --.-KB/s    in 0s      

2024-03-03 23:17:28 (371 MB/s) - 'level2.py' saved [914/914]

edwin2809-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/15/level2.flag.txt.enc
--2024-03-03 23:17:39--  https://artifacts.picoctf.net/c/15/level2.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.92, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level2.flag.txt.enc'

level2.flag.txt.enc                                     100%[===============================================================================================================================>]      31  --.-KB/s    in 0s      

2024-03-03 23:17:39 (11.9 MB/s) - 'level2.flag.txt.enc' saved [31/31]

edwin2809-picoctf@webshell:~$ nano level2.
level2.flag.txt.enc  level2.py            
edwin2809-picoctf@webshell:~$ nano level2.py 
edwin2809-picoctf@webshell:~$ python3 level2.py
Please enter correct password for flag: 39ce
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_502ec42e}
edwin2809-picoctf@webshell:~$ 
El valor ASCII de la cadena resultante de concatenar los caracteres es: 39ce.
```
## Notas adicionales
if( user_pw == chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65) ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
## Referencias

