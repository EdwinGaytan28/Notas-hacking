## Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/16/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/16/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/16/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Solución
```
edwin2809-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/16/level3.py
--2024-03-03 23:24:05--  https://artifacts.picoctf.net/c/16/level3.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.92, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1337 (1.3K) [application/octet-stream]
Saving to: 'level3.py'

level3.py                                               100%[===============================================================================================================================>]   1.31K  --.-KB/s    in 0s      

2024-03-03 23:24:05 (484 MB/s) - 'level3.py' saved [1337/1337]

edwin2809-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/16/level3.flag.txt.enc
--2024-03-03 23:24:23--  https://artifacts.picoctf.net/c/16/level3.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.92, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level3.flag.txt.enc'

level3.flag.txt.enc                                     100%[===============================================================================================================================>]      31  --.-KB/s    in 0s      

2024-03-03 23:24:23 (17.4 MB/s) - 'level3.flag.txt.enc' saved [31/31]

edwin2809-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/16/level3.hash.bin
--2024-03-03 23:25:07--  https://artifacts.picoctf.net/c/16/level3.hash.bin
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.43, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16 [application/octet-stream]
Saving to: 'level3.hash.bin'

level3.hash.bin                                         100%[===============================================================================================================================>]      16  --.-KB/s    in 0s      

2024-03-03 23:25:08 (7.88 MB/s) - 'level3.hash.bin' saved [16/16]

edwin2809-picoctf@webshell:~$ nano level3.py 
edwin2809-picoctf@webshell:~$ python3 level3.py 
Please enter correct password for flag: 6997
That password is incorrect
edwin2809-picoctf@webshell:~$ python3 level3.py 
Please enter correct password for flag: 3ac8
That password is incorrect
edwin2809-picoctf@webshell:~$ python3 level3.py 
Please enter correct password for flag: f0ac
That password is incorrect
edwin2809-picoctf@webshell:~$ python3 level3.py 
Please enter correct password for flag: 4b17
That password is incorrect
edwin2809-picoctf@webshell:~$ python3 level3.py 
Please enter correct password for flag: ec27
That password is incorrect
edwin2809-picoctf@webshell:~$ python3 level3.py 
Please enter correct password for flag: 4e66
That password is incorrect
edwin2809-picoctf@webshell:~$ python3 level3.py 
Please enter correct password for flag: 865e
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_2b072a90}
edwin2809-picoctf@webshell:~$
```
## Notas adicionales
pos_pw_list = ["6997", "3ac8", "f0ac", "4b17", "ec27", "4e66", "865e"]

## Referencias

