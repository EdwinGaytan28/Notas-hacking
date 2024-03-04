## Objetivo
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/515f19f3612bfd97cd3f0c0ba32bd864/file)? This would be really tedious to look through manually, something tells me there is a better way.
## Solución
```
edwin2809-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/515f19f3612bfd97cd3f0c0ba32bd864/file
--2024-03-03 21:35:48--  https://jupiter.challenges.picoctf.org/static/515f19f3612bfd97cd3f0c0ba32bd864/file
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 14551 (14K) [application/octet-stream]
Saving to: 'file'

file                        100%[=========================================>]  14.21K  --.-KB/s    in 0s      

2024-03-03 21:35:48 (410 MB/s) - 'file' saved [14551/14551]

edwin2809-picoctf@webshell:~$ ls -la
total 168
drwxr-xr-x 4 edwin2809-picoctf edwin2809-picoctf  4096 Mar  3 21:35 .
drwxr-xr-x 3 root              root                 31 Feb 27 18:18 ..
-rw------- 1 edwin2809-picoctf edwin2809-picoctf    96 Feb 27 19:29 .bash_history
-rw-r--r-- 1 edwin2809-picoctf edwin2809-picoctf   220 Feb 27 18:18 .bash_logout
-rw-r--r-- 1 edwin2809-picoctf edwin2809-picoctf  3771 Feb 27 18:18 .bashrc
-rw------- 1 edwin2809-picoctf edwin2809-picoctf    20 Feb 27 18:25 .lesshst
-rw-r--r-- 1 edwin2809-picoctf edwin2809-picoctf   807 Feb 27 18:18 .profile
-rw------- 1 edwin2809-picoctf edwin2809-picoctf    37 Mar  3 21:08 .python_history
drwx------ 2 edwin2809-picoctf edwin2809-picoctf    48 Feb 27 18:58 .ssh
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf   215 Mar  3 21:35 .wget-hsts
drwxr-xr-x 3 edwin2809-picoctf edwin2809-picoctf    28 Mar 16  2021 Addadshashanammu
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  4519 Mar 16  2021 Addadshashanammu.zip
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  4519 Mar 16  2021 Addadshashanammu.zip.1
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  4519 Mar 16  2021 Addadshashanammu.zip.2
-rw-r--r-- 1 root              root               4443 Mar  3 20:44 README.txt
-rwxrwxr-x 1 edwin2809-picoctf edwin2809-picoctf  1278 Mar 16  2023 code.py
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf    27 Mar 16  2023 codebook.txt
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  1189 Mar 16  2023 convertme.py
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf 14551 Oct 26  2020 file
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf    34 Mar 16  2021 flag
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf    34 Mar 16  2021 flag.1
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf   785 Mar 16  2021 ltdis.sh
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf   785 Mar 16  2021 ltdis.sh.1
-rwxrwxr-x 1 edwin2809-picoctf edwin2809-picoctf  8376 Mar 16  2021 static
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  8376 Mar 16  2021 static.1
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  8376 Mar 16  2021 static.2
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  8376 Mar 16  2021 static.3
-rwxrwxr-x 1 edwin2809-picoctf edwin2809-picoctf 10936 Mar 16  2021 warm
edwin2809-picoctf@webshell:~$ cat file | grep pico 
picoCTF{grep_is_good_to_find_things_5af9d829}
edwin2809-picoctf@webshell:~$ 

```
## Notas adicionales

## Referencias

