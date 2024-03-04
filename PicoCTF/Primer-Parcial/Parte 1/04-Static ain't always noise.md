## Objetivo
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/static)? This [BASH script](https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/ltdis.sh) might help!
## Solución
```
edwin2809-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/static
--2024-03-04 01:46:38--  https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/static
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 8376 (8.2K) [application/octet-stream]
Saving to: 'static.5'

static.5                    100%[=========================================>]   8.18K  --.-KB/s    in 0s      

2024-03-04 01:46:38 (234 MB/s) - 'static.5' saved [8376/8376]

edwin2809-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/ltdis.sh
--2024-03-04 01:46:48--  https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/ltdis.sh
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 785 [application/octet-stream]
Saving to: 'ltdis.sh.3'

ltdis.sh.3                  100%[=========================================>]     785  --.-KB/s    in 0s      

2024-03-04 01:46:48 (304 MB/s) - 'ltdis.sh.3' saved [785/785]
edwin2809-picoctf@webshell:~$ strings static.5 | grep pico
picoCTF{d15a5m_t34s3r_6f8c8200}
edwin2809-picoctf@webshell:~$ 
```
## Notas adicionales

## Referencias
