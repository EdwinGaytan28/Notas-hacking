## Objetivo
Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin. Login via `ssh` as `ctf-player` with the password, `a13b7f9d`
## Solución
```
(kali㉿kali)-[~]
└─$ ssh ctf-player@venus.picoctf.net -p 54223        
The authenticity of host '[venus.picoctf.net]:54223 ([3.131.124.143]:54223)' can't be established.
ED25519 key fingerprint is SHA256:P1f6h95BrSVnJbm2AKhphfHHGEyAeThib/rN/AwKs24.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[venus.picoctf.net]:54223' (ED25519) to the list of known hosts.
ctf-player@venus.picoctf.net's password: 
Welcome to Ubuntu 18.04.5 LTS (GNU/Linux 5.4.0-1041-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage
This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.
Last login: Tue Feb 27 18:58:37 2024 from 127.0.0.1
ctf-player@pico-chall$ ls -ls
total 8
4 -rw-r--r-- 1 ctf-player ctf-player 14 Mar 16  2021 1of3.flag.txt
4 -rw-r--r-- 1 ctf-player ctf-player 56 Mar 16  2021 instructions-to-2of3.txt
ctf-player@pico-chall$ cat 1of3.flag.txt 
picoCTF{xxsh_
ctf-player@pico-chall$ cat instructions-to-2of3.txt 
Next, go to the root of all things, more succinctly `/`
ctf-player@pico-chall$ ls -la
total 16
drwxr-xr-x 1 ctf-player ctf-player 4096 Mar 16  2021 .
drwxr-xr-x 1 ctf-player ctf-player 4096 Feb 27 18:58 ..
-rw-r--r-- 1 ctf-player ctf-player   14 Mar 16  2021 1of3.flag.txt
-rw-r--r-- 1 ctf-player ctf-player   56 Mar 16  2021 instructions-to-2of3.txt
ctf-player@pico-chall$ cd /
ctf-player@pico-chall$ cat .dockerenv
ctf-player@pico-chall$ cat 2of3.flag.txt 
0ut_0f_\/\/4t3r_
ctf-player@pico-chall$ cd
ctf-player@pico-chall$ ls -la
total 32
drwxr-xr-x 1 ctf-player ctf-player 4096 Feb 27 18:58 .
drwxr-xr-x 1 root       root       4096 Mar 16  2021 ..
drwx------ 2 ctf-player ctf-player 4096 Feb 27 18:58 .cache
-rw-r--r-- 1 ctf-player ctf-player   80 Mar 16  2021 .profile
drw------- 1 ctf-player ctf-player 4096 Mar 16  2021 .ssh
-rw-r--r-- 1 ctf-player ctf-player   10 Mar 16  2021 3of3.flag.txt
drwxr-xr-x 1 ctf-player ctf-player 4096 Mar 16  2021 drop-in
ctf-player@pico-chall$ cat ^C
ctf-player@pico-chall$ cat 3of3.flag.txt 
71be5264}
ctf-player@pico-chall$ ^C
ctf-player@pico-chall$ Connection to venus.picoctf.net closed by remote host.
Connection to venus.picoctf.net closed.

picoCTF{xxsh_0ut_0f_\/\/4t3r_71be5264}
```
## Notas adicionales

## Referencias
