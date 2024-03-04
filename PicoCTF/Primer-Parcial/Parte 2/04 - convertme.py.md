
## Objetivo
Run the Python script and convert the given number from decimal to binary to get the flag.[Download Python script](https://artifacts.picoctf.net/c/22/convertme.py)
## Solución
```
edwin2809-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/22/convertme.py
--2024-03-03 21:28:30--  https://artifacts.picoctf.net/c/22/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.43, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: 'convertme.py'

convertme.py                                            100%[===============================================================================================================================>]   1.16K  --.-KB/s    in 0s      

2024-03-03 21:28:30 (61.4 MB/s) - 'convertme.py' saved [1189/1189]

edwin2809-picoctf@webshell:~$ ls -la
total 152
drwxr-xr-x 4 edwin2809-picoctf edwin2809-picoctf  4096 Mar  3 21:28 .
drwxr-xr-x 3 root              root                 31 Feb 27 18:18 ..
-rw------- 1 edwin2809-picoctf edwin2809-picoctf    96 Feb 27 19:29 .bash_history
-rw-r--r-- 1 edwin2809-picoctf edwin2809-picoctf   220 Feb 27 18:18 .bash_logout
-rw-r--r-- 1 edwin2809-picoctf edwin2809-picoctf  3771 Feb 27 18:18 .bashrc
-rw------- 1 edwin2809-picoctf edwin2809-picoctf    20 Feb 27 18:25 .lesshst
-rw-r--r-- 1 edwin2809-picoctf edwin2809-picoctf   807 Feb 27 18:18 .profile
-rw------- 1 edwin2809-picoctf edwin2809-picoctf    37 Mar  3 21:08 .python_history
drwx------ 2 edwin2809-picoctf edwin2809-picoctf    48 Feb 27 18:58 .ssh
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf   167 Feb 27 18:24 .wget-hsts
drwxr-xr-x 3 edwin2809-picoctf edwin2809-picoctf    28 Mar 16  2021 Addadshashanammu
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  4519 Mar 16  2021 Addadshashanammu.zip
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  4519 Mar 16  2021 Addadshashanammu.zip.1
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  4519 Mar 16  2021 Addadshashanammu.zip.2
-rw-r--r-- 1 root              root               4443 Mar  3 20:44 README.txt
-rwxrwxr-x 1 edwin2809-picoctf edwin2809-picoctf  1278 Mar 16  2023 code.py
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf    27 Mar 16  2023 codebook.txt
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  1189 Mar 16  2023 convertme.py
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf    34 Mar 16  2021 flag
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf    34 Mar 16  2021 flag.1
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf   785 Mar 16  2021 ltdis.sh
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf   785 Mar 16  2021 ltdis.sh.1
-rwxrwxr-x 1 edwin2809-picoctf edwin2809-picoctf  8376 Mar 16  2021 static
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  8376 Mar 16  2021 static.1
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  8376 Mar 16  2021 static.2
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  8376 Mar 16  2021 static.3
-rwxrwxr-x 1 edwin2809-picoctf edwin2809-picoctf 10936 Mar 16  2021 warm
edwin2809-picoctf@webshell:~$ python3 convertme.py 
If 36 is in decimal base, what is it in binary base?
Answer: 100100
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_762f748e}
edwin2809-picoctf@webshell:~$ 
```
## Notas adicionales
Convertimos 36 a binario y es 100100
## Referencias

