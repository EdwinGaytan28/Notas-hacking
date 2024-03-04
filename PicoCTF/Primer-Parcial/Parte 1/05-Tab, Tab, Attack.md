## Objetivo
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames:
## Solución
```
edwin2809-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/9689f2b453ad5daeb73ca7534e4d1521/Addadshashanammu.zip
--2024-03-03 20:44:19--  https://mercury.picoctf.net/static/9689f2b453ad5daeb73ca7534e4d1521/Addadshashanammu.zip
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 4519 (4.4K) [application/octet-stream]
Saving to: 'Addadshashanammu.zip.2'

Addadshashanammu.zip.2                                  100%[===============================================================================================================================>]   4.41K  --.-KB/s    in 0s      

2024-03-03 20:44:19 (1.36 GB/s) - 'Addadshashanammu.zip.2' saved [4519/4519]

edwin2809-picoctf@webshell:~$ ls -la
total 84
drwxr-xr-x 4 edwin2809-picoctf edwin2809-picoctf  4096 Mar  3 20:44 .
drwxr-xr-x 3 root              root                 31 Feb 27 18:18 ..
-rw------- 1 edwin2809-picoctf edwin2809-picoctf    96 Feb 27 19:29 .bash_history
-rw-r--r-- 1 edwin2809-picoctf edwin2809-picoctf   220 Feb 27 18:18 .bash_logout
-rw-r--r-- 1 edwin2809-picoctf edwin2809-picoctf  3771 Feb 27 18:18 .bashrc
-rw------- 1 edwin2809-picoctf edwin2809-picoctf    20 Feb 27 18:25 .lesshst
-rw-r--r-- 1 edwin2809-picoctf edwin2809-picoctf   807 Feb 27 18:18 .profile
-rw------- 1 edwin2809-picoctf edwin2809-picoctf    22 Feb 27 18:57 .python_history
drwx------ 2 edwin2809-picoctf edwin2809-picoctf    48 Feb 27 18:58 .ssh
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf   167 Feb 27 18:24 .wget-hsts
drwxr-xr-x 3 edwin2809-picoctf edwin2809-picoctf    28 Mar 16  2021 Addadshashanammu
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  4519 Mar 16  2021 Addadshashanammu.zip
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  4519 Mar 16  2021 Addadshashanammu.zip.1
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  4519 Mar 16  2021 Addadshashanammu.zip.2
-rw-r--r-- 1 root              root               4443 Mar  3 20:44 README.txt
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf    34 Mar 16  2021 flag
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf    34 Mar 16  2021 flag.1
-rwxrwxr-x 1 edwin2809-picoctf edwin2809-picoctf 10936 Mar 16  2021 warm
edwin2809-picoctf@webshell:~$ unzip Addadshashanammu.zip 
Archive:  Addadshashanammu.zip
replace Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet? [y]es, [n]o, [A]ll, [N]one, [r]ename: y
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  
edwin2809-picoctf@webshell:~$ ls -la
total 84
drwxr-xr-x 4 edwin2809-picoctf edwin2809-picoctf  4096 Mar  3 20:44 .
drwxr-xr-x 3 root              root                 31 Feb 27 18:18 ..
-rw------- 1 edwin2809-picoctf edwin2809-picoctf    96 Feb 27 19:29 .bash_history
-rw-r--r-- 1 edwin2809-picoctf edwin2809-picoctf   220 Feb 27 18:18 .bash_logout
-rw-r--r-- 1 edwin2809-picoctf edwin2809-picoctf  3771 Feb 27 18:18 .bashrc
-rw------- 1 edwin2809-picoctf edwin2809-picoctf    20 Feb 27 18:25 .lesshst
-rw-r--r-- 1 edwin2809-picoctf edwin2809-picoctf   807 Feb 27 18:18 .profile
-rw------- 1 edwin2809-picoctf edwin2809-picoctf    22 Feb 27 18:57 .python_history
drwx------ 2 edwin2809-picoctf edwin2809-picoctf    48 Feb 27 18:58 .ssh
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf   167 Feb 27 18:24 .wget-hsts
drwxr-xr-x 3 edwin2809-picoctf edwin2809-picoctf    28 Mar 16  2021 Addadshashanammu
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  4519 Mar 16  2021 Addadshashanammu.zip
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  4519 Mar 16  2021 Addadshashanammu.zip.1
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf  4519 Mar 16  2021 Addadshashanammu.zip.2
-rw-r--r-- 1 root              root               4443 Mar  3 20:44 README.txt
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf    34 Mar 16  2021 flag
-rw-rw-r-- 1 edwin2809-picoctf edwin2809-picoctf    34 Mar 16  2021 flag.1
-rwxrwxr-x 1 edwin2809-picoctf edwin2809-picoctf 10936 Mar 16  2021 warm
edwin2809-picoctf@webshell:~$ cd Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ./fang-of-haynekhtnamet
-bash: cd: too many arguments
edwin2809-picoctf@webshell:~$ cd Addadshashanammu/Almurbalarammi//Ashalmimilkala//Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
edwin2809-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ls
fang-of-haynekhtnamet
edwin2809-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ls -la
total 12
drwxr-xr-x 2 edwin2809-picoctf edwin2809-picoctf   35 Mar  3 20:45 .
drwxr-xr-x 3 edwin2809-picoctf edwin2809-picoctf   27 Mar 16  2021 ..
-rwxr-xr-x 1 edwin2809-picoctf edwin2809-picoctf 8320 Mar 16  2021 fang-of-haynekhtnamet
edwin2809-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ./fang-of-haynekhtnamet
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_2bcfb2ab}
edwin2809-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ^C
edwin2809-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ 
```
## Notas adicionales

## Referencias
