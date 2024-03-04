## Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/10/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/10/level1.flag.txt.enc) in the same directory too.
## Solución
```
edwin2809-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/10/level1.py
--2024-03-03 22:19:38--  https://artifacts.picoctf.net/c/10/level1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.128, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 876 [application/octet-stream]
Saving to: 'level1.py'

level1.py                                               100%[===============================================================================================================================>]     876  --.-KB/s    in 0.001s  

2024-03-03 22:19:39 (1.12 MB/s) - 'level1.py' saved [876/876]

edwin2809-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/10/level1.flag.txt.enc
--2024-03-03 22:19:55--  https://artifacts.picoctf.net/c/10/level1.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.92, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 30 [application/octet-stream]
Saving to: 'level1.flag.txt.enc'

level1.flag.txt.enc                                     100%[===============================================================================================================================>]      30  --.-KB/s    in 0s      

2024-03-03 22:19:55 (1.39 MB/s) - 'level1.flag.txt.enc' saved [30/30]

edwin2809-picoctf@webshell:~$ ls -la
total 948
drwxr-xr-x 5 edwin2809-picoctf edwin2809-picoctf   4096 Mar  3 22:19 .
drwxr-xr-x 3 root              root                  31 Feb 27 18:18 ..
-rw------- 1 edwin2809-picoctf edwin2809-picoctf     96 Feb 27 19:29 .bash_history
-rw-r--r-- 1 edwin2809-picoctf edwin2809-picoctf    220 Feb 27 18:18 .bash_logout
-rw-r--r-- 1 edwin2809-picoctf edwin2809-picoctf   3771 Feb 27 18:18 .bashrc
-rw------- 1 edwin2809-picoctf edwin2809-picoctf     20 Feb 27 18:25 .lesshst
drwxrwxr-x 3 edwin2809-picoctf edwin2809-picoctf     19 Mar  3 21:42 .local
-rw-r--r-- 1 edwin2809-picoctf edwin2809-picoctf    807 Feb 27 18:18 .profile
-rw------- 1 edwin2809-picoctf edwin2809-picoctf     37 Mar  3 21:08 .python_history
drwx------ 2 edwin2809-picoctf edwin2809-picoctf     48 Feb 27 18:58 .ssh
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf    167 Mar  3 21:58 .wget-hsts
drwxr-xr-x 3 edwin2809-picoctf edwin2809-picoctf     28 Mar 16  2021 Addadshashanammu
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf   4519 Mar 16  2021 Addadshashanammu.zip
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf   4519 Mar 16  2021 Addadshashanammu.zip.1
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf   4519 Mar 16  2021 Addadshashanammu.zip.2
-rw-r--r-- 1 root              root                4443 Mar  3 21:47 README.txt
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf      0 Mar  3 22:07 ]
-rwxrwxr-x 1 edwin2809-picoctf edwin2809-picoctf   1278 Mar 16  2023 code.py
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf     27 Mar 16  2023 codebook.txt
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf   1189 Mar 16  2023 convertme.py
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  14551 Oct 26  2020 file
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf    837 Mar  3 21:54 fixme1.py
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf    837 Mar 16  2023 fixme1.py.1
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf   1030 Mar  3 22:06 fixme2.py
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf     34 Mar 16  2021 flag
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf     34 Mar 16  2021 flag.1
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf     30 Mar 16  2023 level1.flag.txt.enc
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf    876 Mar 16  2023 level1.py
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf    785 Mar 16  2021 ltdis.sh
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf    785 Mar 16  2021 ltdis.sh.1
-rwxrwxr-x 1 edwin2809-picoctf edwin2809-picoctf   8376 Mar 16  2021 static
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf   8376 Mar 16  2021 static.1
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf   8376 Mar 16  2021 static.2
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf   8376 Mar 16  2021 static.3
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf 776032 Oct 26  2020 strings
-rwxrwxr-x 1 edwin2809-picoctf edwin2809-picoctf  10936 Mar 16  2021 warm
edwin2809-picoctf@webshell:~$ nano level1.py 
edwin2809-picoctf@webshell:~$ python3 level1.py 
Please enter correct password for flag: 691d
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_56891419}
edwin2809-picoctf@webshell:~$ 
```
## Notas adicionales
if( user_pw == "691d"):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")
## Referencias

