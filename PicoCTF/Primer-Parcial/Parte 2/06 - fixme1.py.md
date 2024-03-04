## Objetivo
Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/27/fixme1.py)
## Solución
```
edwin2809-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/27/fixme1.py
--2024-03-03 21:48:17--  https://artifacts.picoctf.net/c/27/fixme1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.16, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 837 [application/octet-stream]
Saving to: 'fixme1.py.1'

fixme1.py.1                                             100%[===============================================================================================================================>]     837  --.-KB/s    in 0s      

2024-03-03 21:48:17 (34.4 MB/s) - 'fixme1.py.1' saved [837/837]

edwin2809-picoctf@webshell:~$ ls -la
total 180
drwxr-xr-x 5 edwin2809-picoctf edwin2809-picoctf  4096 Mar  3 21:48 .
drwxr-xr-x 3 root              root                 31 Feb 27 18:18 ..
-rw------- 1 edwin2809-picoctf edwin2809-picoctf    96 Feb 27 19:29 .bash_history
-rw-r--r-- 1 edwin2809-picoctf edwin2809-picoctf   220 Feb 27 18:18 .bash_logout
-rw-r--r-- 1 edwin2809-picoctf edwin2809-picoctf  3771 Feb 27 18:18 .bashrc
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  1024 Mar  3 21:46 .fixme1.py.swp
-rw------- 1 edwin2809-picoctf edwin2809-picoctf    20 Feb 27 18:25 .lesshst
drwxrwxr-x 3 edwin2809-picoctf edwin2809-picoctf    19 Mar  3 21:42 .local
-rw-r--r-- 1 edwin2809-picoctf edwin2809-picoctf   807 Feb 27 18:18 .profile
-rw------- 1 edwin2809-picoctf edwin2809-picoctf    37 Mar  3 21:08 .python_history
drwx------ 2 edwin2809-picoctf edwin2809-picoctf    48 Feb 27 18:58 .ssh
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf   215 Mar  3 21:35 .wget-hsts
drwxr-xr-x 3 edwin2809-picoctf edwin2809-picoctf    28 Mar 16  2021 Addadshashanammu
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  4519 Mar 16  2021 Addadshashanammu.zip
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  4519 Mar 16  2021 Addadshashanammu.zip.1
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  4519 Mar 16  2021 Addadshashanammu.zip.2
-rw-r--r-- 1 root              root               4443 Mar  3 21:47 README.txt
-rwxrwxr-x 1 edwin2809-picoctf edwin2809-picoctf  1278 Mar 16  2023 code.py
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf    27 Mar 16  2023 codebook.txt
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  1189 Mar 16  2023 convertme.py
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf 14551 Oct 26  2020 file
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf   840 Mar  3 21:46 fixme1.py
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf   837 Mar 16  2023 fixme1.py.1
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf    34 Mar 16  2021 flag
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf    34 Mar 16  2021 flag.1
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf   785 Mar 16  2021 ltdis.sh
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf   785 Mar 16  2021 ltdis.sh.1
-rwxrwxr-x 1 edwin2809-picoctf edwin2809-picoctf  8376 Mar 16  2021 static
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  8376 Mar 16  2021 static.1
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  8376 Mar 16  2021 static.2
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  8376 Mar 16  2021 static.3
-rwxrwxr-x 1 edwin2809-picoctf edwin2809-picoctf 10936 Mar 16  2021 warm
edwin2809-picoctf@webshell:~$ nano fixme1.py
edwin2809-picoctf@webshell:~$ python fixme1.py 
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_182342f7}
```
## Notas adicionales

## Referencias

