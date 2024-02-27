## Objetivo
This file has a flag in plain sight (aka "in-the-clear")
## Solución
```
edwin2809-picoctf@webshell:~$  wget https://mercury.picoctf.net/static/0e428b2db9788d31189329bed089ce98/flag
--2024-02-27 18:31:49--  https://mercury.picoctf.net/static/0e428b2db9788d31189329bed089ce98/flag
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34 [application/octet-stream]
Saving to: 'flag.1'

flag.1              100%[==================>]      34  --.-KB/s    in 0s      

2024-02-27 18:31:49 (3.32 MB/s) - 'flag.1' saved [34/34]

edwin2809-picoctf@webshell:~$ cat flag
picoCTF{s4n1ty_v3r1f13d_2fd6ed29}
edwin2809-picoctf@webshell:~$ 
```
## Notas adicionales
wget- permite descargar archivos de internet 
## Referencias
